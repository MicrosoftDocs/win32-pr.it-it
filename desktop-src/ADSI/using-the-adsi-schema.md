---
title: Utilizzo dello schema ADSI
description: Uno schema definisce l'universo di oggetti archiviati in una directory.
ms.assetid: 140a5dd0-6f50-4f84-8708-45c0f1c6bdc4
ms.tgt_platform: multiple
keywords:
- Utilizzo dello schema ADSI
- ADSI ADSI, uso, schema ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 478104a24d850f79cc52473f3d9e546936c56650
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103872962"
---
# <a name="using-the-adsi-schema"></a>Utilizzo dello schema ADSI

Uno schema definisce l'universo di oggetti archiviati in una directory. In Active Directory, lo schema specifica gli attributi che un oggetto servizio directory può o deve avere. Specifica inoltre l'intervallo di valori e la sintassi degli attributi e se supportano uno o più valori. In breve, lo schema è organizzato in base alle definizioni di classe, alle definizioni degli attributi e alla sintassi degli attributi. ADSI fornisce tre interfacce per la lettura dei dati di attributi, classi e sintassi da uno schema: [**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass), [**IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty)e [**IADsSyntax**](/windows/desktop/api/Iads/nn-iads-iadssyntax).

Active Directory utilizza un set di oggetti dello schema per fornire la gestione dinamica dello schema estensibile. Per ulteriori informazioni su un oggetto sconosciuto, cercare gli oggetti dello schema associati. Per creare una nuova definizione di classe o estenderne una esistente, è possibile creare o estendere gli oggetti dello schema appropriati. Gli oggetti dello schema sono organizzati nel contenitore dello schema di una determinata directory. Per accedere a una classe dello schema dell'oggetto, utilizzare la proprietà [**IADs. Schema**](iads-property-methods.md) dell'oggetto per ottenere la stringa ADsPath e utilizzare tale stringa per eseguire l'associazione a un'interfaccia [**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass) sulla classe dello schema dell'oggetto.

Per determinare le definizioni degli attributi, ovvero l'intervallo di valori, la sintassi e così via, esaminare gli oggetti attributo dello schema per ogni proprietà supportata dall'oggetto servizio directory. Per ulteriori informazioni su come accedere agli oggetti attributo dello schema, vedere [**IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty).

ADSI astrae i dati di sintassi come necessario e consente di usare [**IADsSyntax**](/windows/desktop/api/Iads/nn-iads-iadssyntax) per identificare la sintassi necessaria per rappresentare i dati degli oggetti.

Per ulteriori informazioni sullo schema di Active Directory, vedere [Active Directory schema](/windows/desktop/AD/active-directory-schema). Per esempi di codice da utilizzare per leggere il contenitore dello schema, vedere [lettura dello schema](reading-the-schema.md).

 

 