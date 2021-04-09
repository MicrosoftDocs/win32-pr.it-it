---
description: Quando si usa un'interfaccia Windows Image Acquisition (WIA) in più thread all'interno di un singolo processo, un'applicazione deve fornire il marshalling per tale interfaccia.
ms.assetid: b125b36e-1428-4aa6-b367-eac78291c88e
title: Uso di più thread in un'applicazione WIA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebb1dbfa552e72dc068aff63a0a316d9af680ed1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129390"
---
# <a name="using-multiple-threads-in-a-wia-application"></a>Uso di più thread in un'applicazione WIA

Quando si usa un'interfaccia Windows Image Acquisition (WIA) in più thread all'interno di un singolo processo, un'applicazione deve fornire il marshalling per tale interfaccia. Se un thread crea un puntatore a interfaccia, non è possibile utilizzare tale puntatore in un thread diverso senza eseguire il marshalling.

Se, ad esempio, un thread in un'applicazione ottiene un puntatore all'interfaccia [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) o [**IWiaItem2**](-wia-iwiaitem2.md) , un thread separato non può utilizzare tale puntatore di interfaccia senza marshalling.

Una tecnica comune utilizzata per eseguire questo marshalling consiste nell'utilizzare la tabella dell'interfaccia globale. La tabella dell'interfaccia globale è una tabella mantenuta in tutti i thread all'interno di un singolo processo. Tutti i thread in esecuzione nel processo possono recuperare le interfacce registrate nella tabella dell'interfaccia globale. Questa tecnica evita la necessità di creare flussi per il passaggio di interfacce tra thread.

Per informazioni sull'uso della tabella dell'interfaccia globale, vedere [IGlobalInterfaceTable](/windows/win32/api/objidl/nn-objidl-iglobalinterfacetable).

Anche se non si prevede di usare più thread in un'applicazione WIA, è necessario presupporre che tutte le funzioni di callback degli eventi di trasferimento dati o del dispositivo vengano eseguite in thread distinti.

 

 
