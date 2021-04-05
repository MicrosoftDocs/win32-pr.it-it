---
title: Differenze tra le implementazioni di file autonomi e composti
description: L'implementazione autonoma delle interfacce del set di proprietà e dell'implementazione del file composto differisce in qualche modo.
ms.assetid: 650d4759-a58a-47a4-922d-5757e356cf56
keywords:
- IPropertyStorage Strctd STG, implementazioni
- IPropertyStorage Strctd STG, implementazioni, differenze
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 988f8a9cfdaca0a131bedf98cd8ff10ae8b89525
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855946"
---
# <a name="differences-between-stand-alone-and-compound-file-implementations"></a>Differenze tra le implementazioni di file autonomi e composti

L'implementazione autonoma delle interfacce del set di proprietà e dell'implementazione del file composto differisce in qualche modo. Nell'implementazione del file composto di flusso, archiviazione, archiviazione dei set di proprietà e oggetti di archiviazione delle proprietà, le varie interfacce coordinano tra loro perché condividono un'implementazione comune. Nell'implementazione autonoma, le implementazioni dell'interfaccia sono distinte.

Di conseguenza, l'implementazione del file composto gestisce i problemi di concorrenza e sincronizza l'oggetto set di proprietà con l'oggetto di archiviazione o flusso. Con l'implementazione autonoma, il client è responsabile della gestione dei problemi di concorrenza e di sincronizzazione tra l'oggetto di archiviazione o flusso e il set di proprietà. Un client può soddisfare questi requisiti seguendo due semplici regole. Prima di tutto, non modificare mai un set di proprietà usando le interfacce di flusso o di archiviazione mentre un oggetto di archiviazione delle proprietà è aperto. In secondo luogo, chiamare sempre **commit** su un oggetto di archiviazione della proprietà prima di chiamare **CopyTo**, **MoveElementTo** o **commit** su un oggetto di archiviazione predecessore. In particolare, per i seguenti elementi è richiesta l'attenzione del client:

-   Nell'implementazione del file composto, un singolo meccanismo fornisce la protezione della concorrenza per l'oggetto di archiviazione e i relativi oggetti del set di proprietà associati. Tuttavia, nell'implementazione autonoma, l'implementazione dell'oggetto di archiviazione è separata dall'implementazione del set di proprietà e ognuno fornisce i propri meccanismi di concorrenza. Nell'implementazione autonoma, quindi, il client è responsabile della gestione della protezione della concorrenza tra le due implementazioni tramite un meccanismo di esclusione reciproca.
-   Nell'implementazione del file composto le modifiche apportate ai set di proprietà vengono memorizzate nel buffer in una cache di set di proprietà. Quindi, quando il metodo [**IStorage:: commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit) viene chiamato sull'oggetto di archiviazione, l'implementazione dei file composti Scarica automaticamente le modifiche del set di proprietà dal buffer del set di proprietà prima del commit dell'oggetto di archiviazione. Pertanto, le modifiche apportate al set di proprietà vengono rese visibili come parte della transazione di cui viene eseguito il commit.

    Nell'implementazione autonoma, il client deve svuotare in modo esplicito il buffer del set di proprietà chiamando [**IPropertyStorage:: commit**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-commit) prima di chiamare il metodo [**IStorage:: commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit) sull'archiviazione. In alternativa, il client può utilizzare il nuovo \_ valore non memorizzato nel buffer di PROPSETFLAG nell'implementazione autonoma per scrivere direttamente nel set di proprietà anziché memorizzare nella cache le modifiche apportate al buffer interno del set di proprietà. Se \_ viene usato PROPSETFLAG non memorizzato nel buffer, le responsabilità del client vengono soddisfatte automaticamente. L'implementazione del file composto non supporta il valore non memorizzato nel BUFFER di PROPSETFLAG \_ . Per altre informazioni, vedere [**costanti PROPSETFLAG**](propsetflag-constants.md).

-   Come con le archiviazioni transazionali, l'implementazione del file composto aggiorna il set di proprietà scaricando il buffer interno prima di eseguire una chiamata a [**IStorage:: CopyTo**](/windows/desktop/api/Objidl/nf-objidl-istorage-copyto) o [**IStorage:: MoveElementTo**](/windows/desktop/api/Objidl/nf-objidl-istorage-moveelementto). Pertanto, le modifiche apportate al set di proprietà vengono riflesse nell'elemento di archiviazione copiato o spostato.

    Nell'implementazione autonoma, il client deve svuotare in modo esplicito il buffer del set di proprietà chiamando [**IPropertyStorage:: commit**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-commit) prima di chiamare [**IStorage:: CopyTo**](/windows/desktop/api/Objidl/nf-objidl-istorage-copyto) o [**IStorage:: MoveElementTo**](/windows/desktop/api/Objidl/nf-objidl-istorage-moveelementto). In alternativa, il client può utilizzare il nuovo \_ valore non memorizzato nel buffer di PROPSETFLAG per scrivere direttamente nel set di proprietà anziché memorizzare nella cache le modifiche apportate al buffer del set di proprietà. Per altre informazioni, vedere [**costanti PROPSETFLAG**](propsetflag-constants.md).

 

 




