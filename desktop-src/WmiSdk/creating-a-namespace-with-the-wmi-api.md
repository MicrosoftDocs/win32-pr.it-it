---
description: Un altro modo per creare uno spazio dei nomi è usare l'API WMI per creare lo spazio dei nomi a livello di codice.
ms.assetid: 27a65eb0-4312-4df6-8c74-f30fe61dfec9
ms.tgt_platform: multiple
title: Creazione di uno spazio dei nomi con l'API WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8192bb38b60c3d0ddefb8cc1e5cb7b5f78cb0f5ba7937d39784729e0f61f70b7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119612541"
---
# <a name="creating-a-namespace-with-the-wmi-api"></a>Creazione di uno spazio dei nomi con l'API WMI

Un altro modo per creare uno spazio dei nomi è usare l'API WMI per creare lo spazio dei nomi a livello di codice. Il vantaggio della creazione di uno spazio dei nomi a livello di codice è che è possibile creare lo spazio dei nomi dall'interno di un'applicazione. Tuttavia, l'uso dell'API WMI è più complesso rispetto all'uso di Managed Object Format (MOF) e non è possibile condividere facilmente gli spazi dei nomi con altri sviluppatori.

La procedura seguente descrive come creare uno spazio dei nomi usando l'API WMI.

**Per creare uno spazio dei nomi usando l'API WMI**

1.  Usare [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) per recuperare un puntatore a un [**oggetto IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) che punta alla classe di sistema [**\_ \_ Namespace.**](--namespace.md)
2.  Definire un'istanza della [**\_ \_ classe di**](--namespace.md) sistema Namespace con una chiamata a [**IWbemClassObject::SpawnInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance).
3.  Impostare la **proprietà Name** [**\_ \_ dell'istanza namespace**](--namespace.md) con una chiamata a [**IWbemClassObject::P ut**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put).
4.  Creare lo spazio dei nomi con una chiamata a [**IWbemServices::P utInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance).

    Il *parametro pInst* di [**PutInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) deve puntare alla nuova istanza.

 

 



