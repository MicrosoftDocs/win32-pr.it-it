---
description: La proprietà WindowlessActivation inizializza l'oggetto MSWebDVD in fase di progettazione per la modalità finestra o senza finestra.
ms.assetid: 290a9459-154a-4ec7-a013-d696e6b27341
title: Proprietà WindowlessActivation
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6915dbf2ddcfe1b8925ccc1dc3c163799563d137e39e6d6260ad75f5496a0b1d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119982251"
---
# <a name="windowlessactivation-property"></a>Proprietà WindowlessActivation

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

La `WindowlessActivation` proprietà inizializza **l'oggetto MSWebDVD** in fase di progettazione per la modalità finestra o senza finestra.

``` syntax
[ bWindowless = ] MSWebDVD.WindowlessActivation
```

## <a name="return-value"></a>Valore restituito

Restituisce un valore che indica se l'oggetto è in modalità finestra come valore booleano.

## <a name="remarks"></a>Commenti

Questa proprietà è di lettura/scrittura con il valore predefinito true. Pertanto, è necessario impostare questa proprietà solo se si esegue **l'oggetto MSWebDVD** in un contenitore con finestre. Quando è contenuto in una pagina Web in Microsoft® Internet Explorer, **MSWebDVD** è sempre in modalità senza finestra e non è necessario impostare questa proprietà.

 

 



