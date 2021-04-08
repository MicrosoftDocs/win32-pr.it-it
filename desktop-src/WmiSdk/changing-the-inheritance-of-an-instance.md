---
description: È possibile che si verifichi una situazione in cui un'istanza creata come figlio di una classe padre deve modificare le classi padre e diventare l'elemento figlio di un'altra classe padre.
ms.assetid: 6d0fd456-81ab-4665-bb88-f9fb29fbbd39
ms.tgt_platform: multiple
title: Modifica dell'ereditarietà di un'istanza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a35de3dcc37d91b318ab60fb5a520cb4da10e59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882321"
---
# <a name="changing-the-inheritance-of-an-instance"></a>Modifica dell'ereditarietà di un'istanza

È possibile che si verifichi una situazione in cui un'istanza creata come figlio di una classe padre deve modificare le classi padre e diventare l'elemento figlio di un'altra classe padre. Ad esempio, è possibile avere una classe derivata, **ManualService**, che descrive un servizio manuale e una classe derivata, **autoservice**, che descrive un servizio automatico. Entrambe le classi hanno un numero elevato di proprietà. Non tutte le proprietà sono identiche. Per modificare un servizio da manuale a automatico, è necessario modificare anche l'istanza che rappresenta il servizio da **ManualService** a **autoservice**. Nella versione corrente di WMI non è possibile chiamare il metodo [**IWbemServices::P utinstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) con il parametro *Pint* che punta a un'istanza di **autoservice** e le proprietà chiave che descrivono l'istanza di **ManualService** . In caso contrario, viene eliminata in modo implicito l'istanza di **ManualService** originale. In sostanza, dopo aver stabilito la classe di un'istanza, è possibile modificare solo la classe padre di un'istanza eliminando l'istanza e ricreando l'istanza come istanza della nuova classe padre.

Nella procedura seguente viene descritto come spostare un'istanza di da una classe a un'altra classe.

**Per spostare un'istanza da una classe a un'altra classe**

1.  Eliminare l'istanza dalla classe originale.
2.  Creare l'istanza sotto la nuova classe.

    WMI non consente alle applicazioni di spostare un'istanza creandola nella nuova classe e quindi aggiornarla con la chiave dell'istanza originale.

Per ulteriori informazioni, vedere [modifica delle informazioni sulle classi e sulle istanze](manipulating-class-and-instance-information.md).

 

 



