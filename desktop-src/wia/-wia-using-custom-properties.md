---
description: Utilizzo di proprietà personalizzate.
ms.assetid: 09b30c95-0ce2-401c-a4ae-99c801a2048a
title: Utilizzo di proprietà personalizzate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eca9f8092afa5b8af22080b154fff79a32a6f304
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307324"
---
# <a name="using-custom-properties"></a>Utilizzo di proprietà personalizzate

**Utilizzo di proprietà personalizzate**.

Un driver Windows Image Acquisition (WIA) può definire proprietà personalizzate. I chiamanti possono modificare le proprietà personalizzate in modo analogo alle normali proprietà WIA. Tuttavia, solo l'applicazione o il modulo dell'interfaccia utente personalizzata può accedere a queste proprietà personalizzate.

I driver WIA devono definire le proprietà personalizzate in modo da avere identificatori di proprietà di cui è stato spostato il \_ DEVPROP privato WIA \_ per le proprietà del dispositivo e usare \_ \_ il ITEMPROP privato WIA per le proprietà degli elementi normali, ad esempio all'interno di [IWiaMiniDrv::d rvinititemproperties](https://msdn.microsoft.com/library/ms794131.aspx). Per ulteriori informazioni, vedere [definizione delle proprietà personalizzate](-wia-defining-custom-properties.md).

Esistono due modi per passare parametri personalizzati ai driver WIA.

La prima opzione consiste nell'usare il metodo **IWiaItemExtras:: Escape** (descritto nella documentazione di Platform SDK). Questa operazione è simile al metodo [IStiUSD:: Escape](https://msdn.microsoft.com/library/ms794396.aspx) , ma consente ai chiamanti di usare direttamente WIA, anziché usare i metodi STI. Se si usa **IWiaItemExtras:: Escape**, è possibile passare qualsiasi informazione al driver e il driver può passare le informazioni. Il servizio WIA gestisce solo i buffer passati tra il chiamante e il driver.

La seconda opzione consiste nell'usare proprietà personalizzate. L'utilizzo del metodo **IWiaItemExtras:: Escape** è più flessibile rispetto all'utilizzo di proprietà WIA personalizzate, ma le proprietà WIA personalizzate consentono di archiviare le informazioni nel flusso di proprietà dell'elemento, in modo che il driver possa leggere le informazioni in un secondo momento.

 

 



