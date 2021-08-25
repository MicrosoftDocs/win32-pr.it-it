---
description: ICE86 genera un avviso se il pacchetto usa la proprietà AdminUser nella colonna del database di tipo Condizione. Gli autori di pacchetti devono usare la proprietà Privileged nelle istruzioni condizionali.
ms.assetid: c23c2920-3b8b-4cd1-a570-bdeabcf11436
title: ICE86
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c96e572a99fc31fea540fa4fbaad4179d1e8f2ecadebfcd9222527ca6a4afac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894991"
---
# <a name="ice86"></a>ICE86

ICE86 genera un avviso se il pacchetto usa la [**proprietà AdminUser**](adminuser.md) nella colonna del database di [tipo](condition.md) Condizione. Gli autori di pacchetti devono usare [**la proprietà Privileged**](privileged.md) nelle istruzioni condizionali.

## <a name="result"></a>Risultato

ICE86 invia l'avviso seguente.



| Avviso ICE86                                                                                               | Descrizione                                                            |
|-------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| Proprietà \` %s \` trovata nella colonna \` \` %s. \` %s \` nella riga %s. \`La proprietà \` con privilegi è spesso più appropriata. | [**La proprietà AdminUser**](adminuser.md) è stata usata in un campo Condizione. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento su ICE](ice-reference.md)
</dt> </dl>

 

 



