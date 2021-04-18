---
description: Un altro modo per creare uno spazio dei nomi consiste nell'usare l'API WMI per creare lo spazio dei nomi a livello di codice.
ms.assetid: 27a65eb0-4312-4df6-8c74-f30fe61dfec9
ms.tgt_platform: multiple
title: Creazione di uno spazio dei nomi con l'API WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53054837157df5edea90657f8b68c87b394b6d04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310394"
---
# <a name="creating-a-namespace-with-the-wmi-api"></a>Creazione di uno spazio dei nomi con l'API WMI

Un altro modo per creare uno spazio dei nomi consiste nell'usare l'API WMI per creare lo spazio dei nomi a livello di codice. Il vantaggio della creazione di uno spazio dei nomi a livello di codice è che è possibile creare lo spazio dei nomi dall'interno di un'applicazione. Tuttavia, l'utilizzo dell'API WMI è più complesso rispetto all'utilizzo del codice Managed Object Format (MOF) e non è possibile condividere facilmente gli spazi dei nomi con altri sviluppatori.

Nella procedura riportata di seguito viene descritto come creare uno spazio dei nomi utilizzando l'API WMI.

**Per creare uno spazio dei nomi tramite l'API WMI**

1.  Usare [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) per recuperare un puntatore a un oggetto [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) che punta alla classe di sistema [**\_ \_ dello spazio dei nomi**](--namespace.md) .
2.  Definire un'istanza della classe di sistema [**\_ \_ namespace**](--namespace.md) con una chiamata a [**IWbemClassObject:: SpawnInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance).
3.  Impostare la proprietà **Name** dell'istanza [**\_ \_ dello spazio dei nomi**](--namespace.md) con una chiamata a [**IWbemClassObject::P UT**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put).
4.  Creare lo spazio dei nomi con una chiamata a [**IWbemServices::P utinstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance).

    Il parametro *Pint* di [**PutInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) deve puntare alla nuova istanza.

 

 



