---
description: Non è necessario un Tablet PC per lo sviluppo di applicazioni Tablet PC, ma è necessario un personal computer in grado di eseguire il software elencato più avanti in questo argomento.
ms.assetid: 82034950-78a7-4bab-b449-1b8ea7d90676
title: Ambiente di sviluppo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fefa29a518beaf21aa8b2457abf17d9581075f73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968605"
---
# <a name="the-development-environment"></a>Ambiente di sviluppo

Non è necessario un Tablet PC per lo sviluppo di applicazioni Tablet PC, ma è necessario un personal computer in grado di eseguire il software elencato più avanti in questo argomento.

È consigliabile testare l'applicazione in un Tablet PC effettivo per assicurarsi che tutte le differenze nell'hardware, ad esempio il digitalizzatore con risoluzione superiore, siano rappresentate.

Un tipico sistema di sviluppo minimo è costituito dai componenti hardware e software seguenti.

## <a name="hardware"></a>Hardware

-   8 MB di spazio su disco rigido per un'installazione completa.
-   Un dispositivo di puntamento per l'input. Sono inclusi dispositivi come un mouse, un tablet esterno o un Tablet PC con un digitalizzatore HID.

HID è l'acronimo di Human Interface Device, uno standard per i dispositivi di input. I digitalizzatori conformi non HID sono trattati come un normale mouse, mentre i digitalizzatori conformi a HID hanno una risoluzione più elevata e più metadati sui tratti, ad esempio la pressione, simili a quelli installati nell'hardware di Tablet PC.

## <a name="software"></a>Software

Per sviluppare applicazioni per Tablet PC, è possibile utilizzare i sistemi operativi seguenti:

-   Windows 7
-   Windows Vista
-   Windows Server 2008
-   Windows XP Tablet PC Edition 2005
-   Windows Server 2003
-   Windows XP Professional

Altri elementi necessari:

-   Visual Studio versione 6 con Service Pack 5 o Visual Studio .NET o Visual Studio .NET 2005
-   Microsoft Internet Explorer 6 o versione successiva (scelta consigliata)

### <a name="details-on-developing-on-non-tablet-pc-skus-of-windows"></a>Informazioni dettagliate sullo sviluppo su SKU di Windows non Tablet PC

I componenti della piattaforma Tablet PC possono essere installati in Windows XP Professional con Service Pack 2 o Windows Server 2003. In questi sistemi operativi, l'applicazione può raccogliere input penna con la classe [**InkCollector**](inkcollector-class.md) e può essere testata e sottoposta a debug. Tuttavia, non è disponibile alcun riconoscimento, a meno che non si installi anche Microsoft Windows XP Tablet PC Edition 2005 Recognizer Pack. È possibile scaricare il pacchetto dall'area Download in MSDN.

Dopo aver installato il Windows SDK in un sistema Windows XP Professional o Windows Server 2003, sono disponibili tutti i file di sviluppo necessari per creare applicazioni Ink, ad esempio msinkaut. h per uno sviluppatore COM. Tuttavia, non sarà possibile eseguire o eseguire il debug dell'applicazione in tale sistema fino a quando non si installano i file di Runtime. Nel caso di uno sviluppatore COM, ad esempio, inkobj.dll necessario installare e registrare. Poiché non si dispone di un sistema in cui sono presenti i file della piattaforma, è necessario installare i componenti della piattaforma Tablet PC dal modulo di merge ridistribuibile, mstpcrt. msm, per ottenere i file di runtime nel sistema.

Il modo più semplice per installare i runtime della piattaforma in un sistema Windows XP Professional o Windows 2000 a scopo di sviluppo è compilare il progetto di installazione di esempio fornito con gli esempi di PC portatili e Tablet PC e distribuirlo nel computer di sviluppo.

> [!Note]  
> Per Windows Vista e Windows XP Tablet PC Edition 2005 sono già installati i componenti della piattaforma, pertanto non sono necessari passaggi aggiuntivi per eseguire il debug di applicazioni Tablet PC.

 

I controlli [InkEdit](inkedit-control-reference.md) e [InkPicture](inkpicture-control-reference.md) possono essere utilizzati per raccogliere input penna in Windows 2000 con Service Pack 4 o Windows XP Professional con Service Pack 2 quando i componenti della piattaforma Tablet PC sono presenti installando tablet PC SDK versione 1,7, ma non sono in grado di raccogliere l'input penna nei sistemi non Tablet PC in cui non sono installati i componenti della piattaforma Tablet PC.

Il Windows SDK fornisce tutti i componenti necessari per sviluppare applicazioni Tablet PC su SKU di Windows non tablet. Impostare la seguente chiave del registro di sistema **DWORD** su 1 per raccogliere l'input penna su SKU non Tablet di Windows:

`HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\TabletPC\Controls\EnableInkCollectionOnNonTablets`

Questa chiave è destinata solo a scopi di sviluppo.

 

 



