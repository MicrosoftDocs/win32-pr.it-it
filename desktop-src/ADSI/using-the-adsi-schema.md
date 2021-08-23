---
title: Uso dello schema ADSI
description: Uno schema definisce l'universo degli oggetti archiviati in una directory.
ms.assetid: 140a5dd0-6f50-4f84-8708-45c0f1c6bdc4
ms.tgt_platform: multiple
keywords:
- Uso dello schema ADSI
- ADSI ADSI , using, SCHEMA ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8aaf49f75d026f52c644d06a6fe36e4555841e3e7bf587ffeb1e0277d1e5ac99
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119648821"
---
# <a name="using-the-adsi-schema"></a>Uso dello schema ADSI

Uno schema definisce l'universo degli oggetti archiviati in una directory. In Active Directory lo schema specifica gli attributi che un oggetto del servizio directory può o deve avere. Specifica inoltre l'intervallo di valori e la sintassi degli attributi e indica se supportano valori singoli o multipli. In breve, lo schema è organizzato in base a definizioni di classe, definizioni di attributi e sintassi degli attributi. ADSI fornisce tre interfacce per la lettura di dati di attributi, classi e sintassi da uno schema: [**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass), [**IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty)e [**IADsSyntax**](/windows/desktop/api/Iads/nn-iads-iadssyntax).

Active Directory usa un set di oggetti dello schema per fornire la gestione dinamica degli schemi estendibile. Per altre informazioni su un oggetto sconosciuto, cercare gli oggetti dello schema associati. Per creare una nuova definizione di classe o estendere una definizione di classe esistente, è possibile creare o estendere gli oggetti dello schema appropriati. Gli oggetti dello schema sono organizzati nel contenitore dello schema di una determinata directory. Per accedere a una classe dello schema dell'oggetto, usare la proprietà [**IADs.Schema**](iads-property-methods.md) dell'oggetto per ottenere la stringa ADsPath e usare tale stringa per l'associazione a un'interfaccia [**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass) nella classe dello schema dell'oggetto.

Per determinare le definizioni degli attributi, ad esempio l'intervallo di valori, la sintassi e così via, esaminare gli oggetti attributo dello schema per ogni proprietà supportata dall'oggetto del servizio directory. Per altre informazioni su come accedere agli oggetti attributo dello schema, vedere [**IADsProperty.**](/windows/desktop/api/Iads/nn-iads-iadsproperty)

ADSI astrae i dati della sintassi in base alle esigenze e consente di usare [**IADsSyntax**](/windows/desktop/api/Iads/nn-iads-iadssyntax) per identificare la sintassi necessaria per rappresentare i dati oggetto.

Per altre informazioni sullo schema di Active Directory, vedere [Schema di Active Directory.](/windows/desktop/AD/active-directory-schema) Per esempi di codice da usare per leggere il contenitore dello schema, vedere [Lettura dello schema.](reading-the-schema.md)

 

 