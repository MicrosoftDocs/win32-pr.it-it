---
description: La proprietà DVDAdm fornisce l'accesso all'oggetto MSDVDAdm che contiene i metodi e le proprietà per il salvataggio delle informazioni sull'applicazione e sull'utente.
ms.assetid: eb73a851-7118-42f3-be99-1cf356d2e37a
title: Proprietà DVDAdm
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5adedea036393e68456cfd9f035882ae9c335063030518e808c57bced6d5b5b6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079161"
---
# <a name="dvdadm-property"></a>Proprietà DVDAdm

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

La `DVDAdm` proprietà fornisce l'accesso [all'oggetto MSDVDAdm](msdvdadm-object.md) che contiene metodi e proprietà per il salvataggio delle informazioni sull'applicazione e sull'utente.

``` syntax
        MSWebDVD.DVDAdm
```

## <a name="remarks"></a>Commenti

Questa proprietà è di sola lettura senza alcun valore predefinito. Non è necessario creare un riferimento separato **all'oggetto MSDVDAdm.** Per accedere ai metodi e alle proprietà dell'oggetto , usare la `DVDAdm` proprietà come illustrato nell'esempio seguente.

## <a name="examples"></a>Esempi


```VB
DVD.DVDAdm.DisableScreenSaver = true
```



 

 



