---
description: Uso di proprietà personalizzate.
ms.assetid: 09b30c95-0ce2-401c-a4ae-99c801a2048a
title: Utilizzo di proprietà personalizzate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ee01bc0df80acecec9805ea15cd8da65fa23a441c9c7818a88223aa47b963d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119813631"
---
# <a name="using-custom-properties"></a>Utilizzo di proprietà personalizzate

**Utilizzo di proprietà personalizzate**.

Un driver Windows Image Acquisition (WIA) può definire proprietà personalizzate. I chiamanti possono modificare le proprietà personalizzate esattamente come le normali proprietà WIA. Tuttavia, solo l'applicazione o il modulo dell'interfaccia utente personalizzato può accedere a queste proprietà personalizzate.

I driver WIA devono definire le proprietà personalizzate in modo che gli identificatori di proprietà siano offset da WIA PRIVATE DEVPROP per le proprietà del dispositivo e usare WIA PRIVATE ITEMPROP per le normali proprietà dell'elemento, ad esempio all'interno di \_ \_ \_ \_ [IWiaMiniDrv::d rvInitItemProperties](https://msdn.microsoft.com/library/ms794131.aspx). Per altre informazioni, vedere [Definizione di proprietà personalizzate](-wia-defining-custom-properties.md).

Esistono due modi per passare parametri personalizzati ai driver WIA.

La prima opzione è usare il **metodo IWiaItemExtras::Escape** (descritto nella documentazione di Platform SDK). È simile al metodo [IStiUSD::Escape,](https://msdn.microsoft.com/library/ms794396.aspx) ma consente ai chiamanti di usare direttamente WIA, anziché i metodi STI. Usando **IWiaItemExtras::Escape,** è possibile passare qualsiasi informazione al driver e il driver può passare qualsiasi informazione. Il servizio WIA gestisce solo i buffer passati tra il chiamante e il driver.

La seconda opzione è usare proprietà personalizzate. L'uso del metodo **IWiaItemExtras::Escape** è più flessibile rispetto all'uso di proprietà WIA personalizzate, ma le proprietà WIA personalizzate consentono di archiviare le informazioni nel flusso delle proprietà dell'elemento in modo che il driver possa leggere le informazioni in un altro momento.

 

 



