---
description: Quando si usa un Windows di acquisizione di immagini in più thread all'interno di un singolo processo, un'applicazione deve fornire il marshalling per tale interfaccia.
ms.assetid: b125b36e-1428-4aa6-b367-eac78291c88e
title: Uso di più thread in un'applicazione WIA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 707adbfe6cd24152209e318bed73a0b6d7fee54b6cfa1e8fbcfecac67e272082
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118208007"
---
# <a name="using-multiple-threads-in-a-wia-application"></a>Uso di più thread in un'applicazione WIA

Quando si usa un Windows di acquisizione di immagini in più thread all'interno di un singolo processo, un'applicazione deve fornire il marshalling per tale interfaccia. Se un thread crea un puntatore a interfaccia, non è possibile usare tale puntatore in un thread diverso senza marshalling.

Ad esempio, se un thread in un'applicazione ottiene un puntatore all'interfaccia [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) o [**IWiaItem2,**](-wia-iwiaitem2.md) un thread separato non può usare tale puntatore di interfaccia senza marshalling.

Una tecnica comune usata per eseguire questo marshalling consiste nell'usare la tabella di interfaccia globale. La tabella di interfaccia globale è una tabella gestita in tutti i thread all'interno di un singolo processo. Tutti i thread in esecuzione all'interno del processo possono recuperare le interfacce registrate nella tabella di interfaccia globale. Questa tecnica evita la necessità di creare flussi per il passaggio di interfacce tra thread.

Per informazioni su come usare la tabella di interfaccia globale, vedere [IGlobalInterfaceTable.](/windows/win32/api/objidl/nn-objidl-iglobalinterfacetable)

Anche se non si prevede di usare più thread in un'applicazione WIA, è necessario presupporre che tutte le funzioni di trasferimento dati o callback degli eventi del dispositivo siano eseguite in thread separati.

 

 
