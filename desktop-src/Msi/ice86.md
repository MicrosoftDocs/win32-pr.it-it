---
description: ICE86 genera un avviso se il pacchetto usa la proprietà AdminUser nella colonna database del tipo di condizione. Gli autori di pacchetti devono utilizzare la proprietà Privileged nelle istruzioni condizionali.
ms.assetid: c23c2920-3b8b-4cd1-a570-bdeabcf11436
title: ICE86
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25df1e2a9c3ab610e78efd6f797cb916f0563e31
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347771"
---
# <a name="ice86"></a>ICE86

ICE86 genera un avviso se il pacchetto usa la proprietà [**AdminUser**](adminuser.md) nella colonna database del tipo di [condizione](condition.md) . Gli autori di pacchetti devono utilizzare la proprietà [**Privileged**](privileged.md) nelle istruzioni condizionali.

## <a name="result"></a>Risultato

ICE86 invia il seguente avviso.



| Avviso di ICE86                                                                                               | Descrizione                                                            |
|-------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| Proprietà \` % s \` trovata nella colonna \` % s \` . \` % s \` nella riga% s. \`\`La proprietà Privileged è spesso più appropriata. | La proprietà [**AdminUser**](adminuser.md) è stata usata in un campo condizione. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento ghiaccio](ice-reference.md)
</dt> </dl>

 

 



