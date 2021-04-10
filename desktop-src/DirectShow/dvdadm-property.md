---
description: La proprietà DVDAdm fornisce l'accesso all'oggetto MSDVDAdm che contiene i metodi e le proprietà per il salvataggio delle informazioni sull'applicazione e sull'utente.
ms.assetid: eb73a851-7118-42f3-be99-1cf356d2e37a
title: Proprietà DVDAdm
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c3d81742fc6e643d6ee805a76c14d07d45d1924
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124584"
---
# <a name="dvdadm-property"></a>Proprietà DVDAdm

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

La `DVDAdm` proprietà fornisce l'accesso all'oggetto [MSDVDAdm](msdvdadm-object.md) che contiene i metodi e le proprietà per il salvataggio delle informazioni sull'applicazione e sull'utente.

``` syntax
        MSWebDVD.DVDAdm
```

## <a name="remarks"></a>Commenti

Questa proprietà è di sola lettura e non prevede alcun valore predefinito. Non è necessario creare un riferimento separato all'oggetto **MSDVDAdm** . Per accedere ai metodi e alle proprietà dell'oggetto, usare la `DVDAdm` proprietà come illustrato nell'esempio seguente.

## <a name="examples"></a>Esempi


```VB
DVD.DVDAdm.DisableScreenSaver = true
```



 

 



