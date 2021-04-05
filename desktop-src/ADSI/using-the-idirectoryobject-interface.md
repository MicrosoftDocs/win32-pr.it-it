---
title: Uso dell'interfaccia IDirectoryObject
description: Quando si crea un client ADSI in C o C++ che usa l'associazione anticipata, sarà disponibile una varietà più ampia di tipi di dati ADSI da usare per il client se chiama l'interfaccia IDirectoryObject invece dell'interfaccia IADs.
ms.assetid: d2c706ed-a341-4c49-91da-70230192f055
ms.tgt_platform: multiple
keywords:
- IDirectoryObject ADSI, utilizzo
- ADSI ADSI, utilizzo di, utilizzo dell'interfaccia IDirectoryObject
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3174402a629bc02df2b1fffe07cc8fba1d73193c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707357"
---
# <a name="using-the-idirectoryobject-interface"></a>Uso dell'interfaccia IDirectoryObject

Quando si crea un client ADSI in C o C++ che usa l'associazione anticipata, sarà disponibile una varietà più ampia di tipi di dati ADSI da usare per il client se chiama l'interfaccia [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) invece dell'interfaccia [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) . L'interfaccia **IDirectoryObject** fornisce metodi per supportare un subset delle proprietà di manutenzione di un oggetto e per accedere ai relativi attributi. Nella figura seguente sono illustrate le relazioni tra le strutture di dati.

![strutture di dati dell'interfaccia IDirectoryObject](images/ds2dso.png)

Nella figura precedente, le [**\_ \_ informazioni sull'oggetto di ADS**](/windows/desktop/api/Iads/ns-iads-ads_object_info) della struttura definiscono le proprietà che identificano l'oggetto in base al nome distinto, al nome distinto relativo, al contenitore (DNPadre), al tipo di oggetto (ClassDN) e alla definizione dello schema (SchemaDN). Il descrittore di attributi [**Ads \_ attr \_ info**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) è costituito da un nome, un tipo di dati, una matrice di valori di dati mostrati in [**ADSVALUE**](/windows/desktop/api/Iads/ns-iads-adsvalue)e un flag che indica al servizio directory sottostante di eseguire determinate operazioni sugli attributi descritti in dettaglio nelle [ \_ \_ \* costanti di ADS attr](adsi-constants.md). I tipi di dati per questi attributi includono i tipi di sintassi estesi ADSI, descritti in dettaglio in [**ADSTYPEENUM**](/windows/win32/api/iads/ne-iads-adstypeenum).

 

 




