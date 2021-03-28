---
title: Registro temporaneo (riferimento HLSL VS)
description: Per mantenere i risultati intermedi, viene usato un registro temporaneo del vertex shader.
ms.assetid: 186adff6-0641-4507-9adc-e02cf1cc3ea9
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c3dcaa5ac0c9c1531a1e1f0476d2ef13b4bac509
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/23/2019
ms.locfileid: "104335692"
---
# <a name="temporary-register-hlsl-vs-reference"></a>Registro temporaneo (riferimento HLSL VS)

Per mantenere i risultati intermedi, viene usato un registro temporaneo del vertex shader.

Prima di utilizzare un registro temporaneo, è necessario inizializzarlo. Ogni registro temporaneo dispone di accesso in sola scrittura e di lettura tripla. Ciò significa che una singola istruzione shader può utilizzare fino a tre registri temporanei come input.

Non è possibile usare i valori in un registro temporaneo che rimangono dalle chiamate precedenti del vertex shader.

Un registro è costituito da proprietà che determinano il comportamento di ogni registro.



| Proprietà        | Descrizione                                                                                                                                                                                 |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nome            | r \[ n \] . n è un numero di registro facoltativo. Il valore predefinito è 0 e è il valore utilizzato se non viene specificato alcun valore.                                                                                 |
| Conteggio           | Un massimo di 12 registri.                                                                                                                                                                  |
| Autorizzazioni di I/O | Proprietà di lettura/scrittura. Questo registro può essere letto o scritto dall'API o dallo shader.                                                                                                               |
| Leggere le porte      | Il numero di volte in cui è possibile leggere un registro all'interno di una singola istruzione è 3. Un registro temporaneo è l'unico registro che può essere letto e scritto più di una volta in un'unica istruzione. |



 

Ogni registro temporaneo dispone di accesso in sola scrittura e di lettura tripla. Un'istruzione può pertanto avere fino a tre registri temporanei nel set di operandi di origine di input.

Non è possibile usare alcun valore in un registro temporaneo che rimanga dalla chiamata precedente del vertex shader. I vertex shader che leggono un valore da un registro temporaneo prima di scrivervi non riusciranno a eseguire la chiamata all'API Direct3D per creare il vertex shader.

## <a name="example"></a>Esempio

Di seguito è riportato un esempio di utilizzo di un registro temporaneo:


```
def c4, 0,0,0,1
...
// Decompress position
mov r0.x, v0.x
mov r0.y, c4.w       // 1
mov r0.z, v0.y
mov r0.w, c4.w       // 1

// Compute theta from distance and time
mov r4.xz, r0        // xz
```





| Versioni vertex shader | 1\_1 | 2 \_ 0 | 2 \_ SW | 2 \_ x | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|-------|------|------|-------|
| Registro temporaneo     | x    | x    | x     | x    | x    | x     |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registri vertex shader](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




