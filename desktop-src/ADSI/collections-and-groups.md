---
title: Raccolte e gruppi
description: ADSI utilizza oggetti raccolta per rappresentare qualsiasi set arbitrario di elementi in un servizio directory che possono essere rappresentati utilizzando lo stesso tipo di dati.
ms.assetid: 03257cc9-f354-4e1c-8880-936a7acac3ef
ms.tgt_platform: multiple
keywords:
- ADSI ADSI, utilizzo, raccolte e gruppi
- ADSI Collections
- ADSI per gruppi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9f0f4d699d8dde0c3d70c7449dfe146212b2b30
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103963443"
---
# <a name="collections-and-groups"></a>Raccolte e gruppi

ADSI utilizza oggetti raccolta per rappresentare qualsiasi set arbitrario di elementi in un servizio directory che possono essere rappresentati utilizzando lo stesso tipo di dati. Gli oggetti della raccolta vengono definiti come un set di valori **Variant** , che rappresenta uno dei tipi di dati di automazione validi. Gli oggetti della raccolta possono rappresentare entrambe le informazioni persistenti, ad esempio elenchi di controllo di accesso e informazioni volatili, ad esempio i processi di stampa in una coda di stampa.

La convenzione COM standard per elencare il contenuto di un oggetto raccolta (o contenitore) consiste nel creare un oggetto enumeratore che supporti [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant), che dispone di metodi per scorrere l'elenco di oggetti raccolta. Le interfacce in ADSI che forniscono il metodo **get \_ \_ NewEnum** (si notino i due caratteri di sottolineatura) sono [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer), [**IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers) e [**IADsCollection**](/windows/desktop/api/Iads/nn-iads-iadscollection). ADSI fornisce anche le funzioni di supporto [**ADsBuildEnumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildenumerator) e [**ADsEnumerateNext**](/windows/desktop/api/Adshlp/nf-adshlp-adsenumeratenext) per i programmi C e C++ per semplificare l'enumerazione. I client di automazione usano l'enumerazione in modo implicito quando chiamano **Next** in un ciclo **for** .

I gruppi sono semplicemente raccolte di oggetti che supportano l'interfaccia [**IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers) .

 

 