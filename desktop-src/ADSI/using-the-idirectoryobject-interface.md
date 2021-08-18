---
title: Uso dell'interfaccia IDirectoryObject
description: Quando si crea un client ADSI in C o C++ che usa l'associazione anticipata, sarà disponibile un'ampia gamma di tipi di dati ADSI da usare per il client se chiama l'interfaccia IDirectoryObject anziché l'interfaccia IAD.
ms.assetid: d2c706ed-a341-4c49-91da-70230192f055
ms.tgt_platform: multiple
keywords:
- IDirectoryObject ADSI , con
- ADSI ADSI , tramite l'interfaccia IDirectoryObject
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d085344e5d2d1afe975dd347ff9e9cf4cdad99c1177819e0094b7a83f2219fb8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023084"
---
# <a name="using-the-idirectoryobject-interface"></a>Uso dell'interfaccia IDirectoryObject

Quando si crea un client ADSI in C o C++ che usa l'associazione anticipata, sarà disponibile un'ampia gamma di tipi di dati ADSI da usare per il client se chiama l'interfaccia [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) anziché [**l'interfaccia IAD.**](/windows/desktop/api/Iads/nn-iads-iads) **L'interfaccia IDirectoryObject** fornisce metodi per supportare un subset delle proprietà di manutenzione di un oggetto e per accedere ai relativi attributi. Nella figura seguente vengono illustrate le relazioni tra le strutture di dati.

![Strutture di dati dell'interfaccia idirectoryobject](images/ds2dso.png)

Nella figura precedente la struttura [**ADS \_ OBJECT \_ INFO**](/windows/desktop/api/Iads/ns-iads-ads_object_info) definisce le proprietà che identificano l'oggetto in base al nome distinto, al nome distinto relativo, al contenitore (ParentDN), al tipo di oggetto (ClassDN) e alla definizione dello schema (SchemaDN). Il descrittore di attributi [**ADS \_ ATTR \_ INFO**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) è costituito da un nome, un tipo di dati, una matrice di valori di dati visualizzati in [**ADSVALUE**](/windows/desktop/api/Iads/ns-iads-adsvalue)e un flag che indica al servizio directory sottostante di eseguire determinate operazioni sugli attributi dettagliati nelle costanti [ \_ ATTR \_ \* di ADS.](adsi-constants.md) I tipi di dati per questi attributi includono i tipi di sintassi estesa ADSI, come descritto in dettaglio in [**ADSTYPEENUM.**](/windows/win32/api/iads/ne-iads-adstypeenum)

 

 




