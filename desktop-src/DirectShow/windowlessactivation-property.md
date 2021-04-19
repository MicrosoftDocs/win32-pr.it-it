---
description: La proprietà WindowlessActivation Inizializza l'oggetto MSWebDVD in fase di progettazione per la modalità finestra o senza finestra.
ms.assetid: 290a9459-154a-4ec7-a013-d696e6b27341
title: Proprietà WindowlessActivation
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 427fdcb265d60200bfe8716cd1ece384861fbdf7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317828"
---
# <a name="windowlessactivation-property"></a>Proprietà WindowlessActivation

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

La `WindowlessActivation` Proprietà Inizializza l'oggetto **mswebdvd** in fase di progettazione per la modalità finestra o senza finestra.

``` syntax
[ bWindowless = ] MSWebDVD.WindowlessActivation
```

## <a name="return-value"></a>Valore restituito

Restituisce un valore che indica se l'oggetto è in modalità finestra come valore booleano.

## <a name="remarks"></a>Commenti

Questa proprietà è di lettura/scrittura e il valore predefinito è true. Pertanto, è necessario impostare questa proprietà solo se si esegue l'oggetto **mswebdvd** in un contenitore a finestra. Quando è contenuto in una pagina Web di Microsoft® Internet Explorer, **mswebdvd** è sempre in modalità senza finestra e non è necessario impostare questa proprietà.

 

 



