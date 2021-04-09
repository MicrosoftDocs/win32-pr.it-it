---
title: Oggetti di archiviazione e di flusso per un set di proprietà
description: Il programmatore specifica se un set di proprietà viene archiviato in una risorsa di archiviazione o in un flusso quando viene creato il set di proprietà.
ms.assetid: d0ca649a-d405-4c34-af02-9c2ca8b2790e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4ebd5d03c3b17e02aa47a7a859576b4cc04607a
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/08/2020
ms.locfileid: "104047517"
---
# <a name="storage-and-stream-objects-for-a-property-set"></a>Oggetti di archiviazione e di flusso per un set di proprietà

Il programmatore specifica se un set di proprietà viene archiviato in una risorsa di archiviazione o in un flusso quando viene creato il set di proprietà. Il \_ valore di enumerazione PROPSETFLAG non semplice, passato nel parametro *grfFlags* al metodo [**IPropertySetStorage:: create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) , indica this. L'impostazione della posizione in cui viene archiviato il set di proprietà fornisce controlli dell'applicazione appropriati per l'interoperabilità completa tramite l'interfaccia [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) con il set di proprietà com.

Se \_ viene impostato il flag PROPSETFLAG non semplice, il set di proprietà viene archiviato in un oggetto di archiviazione e i valori di proprietà non semplici possono essere scritti. I valori non semplici includono valori con un **VarType** di \_ archiviazione VT, un \_ flusso VT, un \_ oggetto archiviato VT o un oggetto con \_ \_ flusso VT \_ . Per ulteriori informazioni sui valori **VarType** e su come utilizzarli, vedere la struttura [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) .

Se il \_ flag PROPSETFLAG non semplice non è impostato, nel set di proprietà è possibile scrivere solo valori semplici.

Nell'oggetto di archiviazione di un set di proprietà non semplice, viene creato un flusso denominato contenuto. Questo è il flusso primario del set di proprietà e include tutti i valori di proprietà semplici. I valori di proprietà non semplici (flussi e archivi) vengono archiviati nell'oggetto di archiviazione principale del set di proprietà come sottoflussi e archivi. Ovvero, questi valori non semplici vengono archiviati come elementi di pari livello nel flusso di contenuti. Il nome dei flussi e delle archiviazioni di pari livello è determinato dall'implementazione e viene archiviato nel flusso di contenuto in modo analogo a come viene archiviata una proprietà stringa semplice.

 

 