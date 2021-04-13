---
title: Scelta di un'interfaccia per l'associazione
description: Quando un oggetto directory è associato a, il chiamante specifica il tipo di interfaccia ADSI desiderata.
ms.assetid: 3c86e136-6d82-4baf-9c76-27dac8ad68ac
ms.tgt_platform: multiple
keywords:
- ADSI ADSI, utilizzo, scelta di un'interfaccia per l'associazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 444bd41d1567849d5bf3a85ac3ec22f317ced5d3
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104399714"
---
# <a name="choosing-an-interface-for-binding"></a>Scelta di un'interfaccia per l'associazione

Quando un oggetto directory è associato a, il chiamante specifica il tipo di interfaccia ADSI desiderata. Tutti gli oggetti directory ADSI supportano l'interfaccia [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) . Un oggetto ADSI può supportare anche altre interfacce. Le interfacce effettive supportate dall'oggetto dipendono dalla classe dell'oggetto. Ad esempio, un oggetto utente supporta l'interfaccia [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser) , ma non supporta l'interfaccia [**IADsComputer**](/windows/desktop/api/Iads/nn-iads-iadscomputer) .

I client di automazione devono usare le interfacce **IADs \*** perché queste interfacce sono interfacce duali che forniscono un livello di astrazione maggiore e forniscono dati usando il tipo di dati [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) .

Oltre alle interfacce **\* IADs** , i client C/C++ possono usare le interfacce [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) e [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) . Queste interfacce non sono interfacce duali e non supportano l'automazione. Queste interfacce consentono un maggiore controllo sugli attributi che consentono di recuperare e consentire l'accesso ai dati non elaborati archiviati in una proprietà. Ad esempio, quando viene usato il metodo [**IADs:: Get**](/windows/desktop/api/Iads/nf-iads-iads-get) per recuperare l'attributo **ntSecurityDescriptor** per un oggetto, il metodo **IADs:: Get** fornisce un puntatore a interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) che supporta l'interfaccia [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor) . L'interfaccia **IADsSecurityDescriptor** viene fornita da ADSI per rappresentare un descrittore di sicurezza. In confronto, quando viene usato il metodo [**IDirectoryObject:: GetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-getobjectattributes) per recuperare l'attributo **ntSecurityDescriptor** , **IDirectoryObject:: GetObjectAttributes** fornisce una matrice di byte di cui è possibile eseguire il cast a una struttura di [**\_ descrittori di sicurezza**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) . Le API di sicurezza Win32 possono essere utilizzate con questi dati per modificare il descrittore di sicurezza.

 

 