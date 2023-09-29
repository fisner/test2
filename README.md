const showInfo = (str) => {
const data = str.split('\n');
const rows = data.slice(1, data.length - 1).map((row) => row.split(','));
console.log(`Count: ${rows.length}`);


const cities = rows.map((row) => row[1]);
const uniques =[];
for (let i = 0; i < cities.length; i += 1) {
    if (!uniques.includes(cities[i])) {
        uniques.push(cities[i]);
    }
}
console.log(`Cities: ${uniques.sort().join(', ')}`);


const minmax = rows.map((row) => (row[3].split(' ')));
let min = Infinity;
let max = -Infinity;
for (let i = 0; i < minmax.length; i += 1) {
    if (minmax[i][0] > max) {
        max = minmax[i][0];
    }
    if (minmax[i][0] < min) {
        min = minmax[i][0];
    }
}
console.log(`Calories: max ${max}, min ${min}`);


// Самое выгодное блюдо
const prices = rows.map((row) => Number(row[4]));
console.log(maxTemps);
// вычисляем индекс самого дорогого блюда
const maxTempIndex = maxTemps.indexOf(Math.max(...maxTemps));
console.log(maxTempIndex);
};
// далее индекс подставляем в нужные столбцы

export default showInfo;