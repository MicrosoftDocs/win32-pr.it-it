---
description: Il qualificatore ViewSpaces definisce i nomi e la posizione degli spazi dei nomi in cui si trovano le istanze di origine. È possibile specificare qualsiasi combinazione di spazi dei nomi in computer locali o remoti.
ms.assetid: 15d71bb6-842d-4f5a-b2e3-e9f60f0aea3b
ms.tgt_platform: multiple
title: Qualificatore ViewSpaces
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ViewSpaces
api_type:
- NA
api_location: ''
ms.openlocfilehash: edaec0328d67ad540a12e3393aabf5b973112bbf00f64f735d6a5f64cf338365
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119049899"
---
# <a name="viewspaces-qualifier"></a>Qualificatore ViewSpaces

Il **qualificatore ViewSpaces** definisce i nomi e la posizione degli spazi dei nomi in cui si trovano le istanze di origine. È possibile specificare qualsiasi combinazione di spazi dei nomi in computer locali o remoti.

Nell'esempio seguente vengono elencati due spazi dei nomi nel computer locale.


```mof
ViewSpaces{"\\\\.\\root\\LocalNamespace",
     "\\\\.\\root\\RemoteNamespace"}
```



Il [provider View abbina](view-provider.md) le query di origine nel qualificatore [ViewSources](viewsources-qualifier.md) agli spazi dei nomi elencati nel qualificatore **ViewSpaces** nell'ordine in cui sono elencate le query e gli spazi dei nomi. In genere, esiste una relazione uno-a-uno tra il numero di spazi dei nomi elencati nel qualificatore **ViewSpaces** e le query elencate nel qualificatore **ViewSources.** In alcuni casi, può essere necessario eseguire le query elencate nel qualificatore ViewSources su due o più spazi dei nomi. È possibile usare i due punti "::" per separare più spazi dei nomi che verranno valutati da una delle query nella **matrice ViewSources.**

Nell'esempio seguente la prima query nella matrice [**ViewSources**](viewsources-qualifier.md) verrà eseguita sullo spazio dei nomi nella prima coppia di virgolette, la seconda query per i tre spazi dei nomi nella seconda coppia di virgolette e la terza query per i due spazi dei nomi nella terza coppia di virgolette.


```mof
ViewSpaces
    {
    "\\\\.\\root\\LocalNamespace",

    "\\\\.\\root\\RemoteNamespace1::
        \\\\.\\root\\RemoteNamespace2::
        \\\\.\\root\\RemoteNamespace3",

    "\\\\.\\root\\RemoteNamespace1::
        \\\\.\\root\\RemoteNamespace3"
    }
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>       |
| Server minimo supportato<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Qualificatori specifici del provider di visualizzazione**](qualifiers-specific-to-the-view-provider.md)
</dt> </dl>

 

 




