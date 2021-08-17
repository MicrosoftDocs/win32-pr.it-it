---
description: Non è necessario un Tablet PC per sviluppare applicazioni Tablet PC, ma è necessario un personal computer in grado di eseguire il software elencato più avanti in questo argomento.
ms.assetid: 82034950-78a7-4bab-b449-1b8ea7d90676
title: Ambiente di sviluppo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6d6c0de35fa84ec4ee01b3f25aaefec6ab3470fde83161f7aaf2157197bbf1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118449214"
---
# <a name="the-development-environment"></a>Ambiente di sviluppo

Non è necessario un Tablet PC per sviluppare applicazioni Tablet PC, ma è necessario un personal computer in grado di eseguire il software elencato più avanti in questo argomento.

È consigliabile testare l'applicazione in un Tablet PC effettivo per assicurarsi che tutte le differenze nell'hardware, ad esempio il digitalizzatore con risoluzione più elevata, siano rappresentate.

Un tipico sistema di sviluppo minimo è costituito dall'hardware e dal software seguenti.

## <a name="hardware"></a>Hardware

-   8 MB di spazio su disco rigido per un'installazione completa.
-   Un dispositivo di puntamento per l'input. Sono inclusi dispositivi come un mouse, un tablet esterno o un Tablet PC con un digitalizzatore HID.

HID è l'acronimo di Human Interface Device, uno standard per i dispositivi di input. I digitalizzatori non conformi a HID vengono trattati come un normale mouse, mentre i digitalizzatori conformi a HID hanno una risoluzione più elevata e più metadati sui tratti, ad esempio la pressione, simili a quelli installati nell'hardware tablet PC.

## <a name="software"></a>Software

Per sviluppare applicazioni Tablet PC, è possibile usare i sistemi operativi seguenti:

-   Windows 7
-   Windows Vista
-   Windows Server 2008
-   Windows XP Tablet PC Edition 2005
-   Windows Server 2003
-   Windows XP Professional

Altri elementi necessari:

-   Visual Studio versione 6 con Service Pack 5 o Visual Studio .NET o Visual Studio .NET 2005
-   Microsoft Internet Explorer 6 o versione successiva (scelta consigliata)

### <a name="details-on-developing-on-non-tablet-pc-skus-of-windows"></a>Informazioni dettagliate sullo sviluppo in SKU non Tablet PC di Windows

I componenti della piattaforma Tablet PC possono essere installati Windows XP Professional con Service Pack 2 o Windows Server 2003. In questi sistemi operativi, l'applicazione può raccogliere input penna con la [**classe InkCollector**](inkcollector-class.md) e può essere testata e di cui è possibile eseguire il debug. Tuttavia, non è disponibile alcun riconoscimento a meno che non si installi anche Microsoft Windows XP Tablet PC Edition 2005 Recognizer Pack. È possibile scaricare tale pacchetto dall'Area download su MSDN.

Dopo aver installato Windows SDK in un sistema Professional Professional o Windows Server 2003 di Windows XP, saranno disponibili tutti i file di sviluppo necessari per compilare applicazioni ink, ad esempio msinkaut.h per uno sviluppatore COM. Tuttavia, non sarà possibile eseguire o eseguire il debug dell'applicazione in tale sistema fino a quando non si installano i file di runtime. Ad esempio, nel caso di uno sviluppatore COM, inkobj.dll essere installato e registrato. Poiché non si è in un sistema in cui sono presenti questi file della piattaforma, è necessario installare i componenti della piattaforma Tablet PC dal modulo unione ridistribuibile mstpcrt.msm per ottenere i file di runtime nel sistema.

Il modo più semplice per installare i runtime della piattaforma in un sistema Windows XP Professional o Windows 2000 a scopo di sviluppo è compilare il progetto di installazione di esempio fornito con gli esempi di PC per dispositivi mobili e Tablet PC e distribuirlo nel computer di sviluppo.

> [!Note]  
> Windows Vista e Windows XP Tablet PC Edition 2005 hanno già installato i componenti della piattaforma, quindi non richiedono passaggi aggiuntivi per l'esecuzione e il debug di applicazioni Tablet PC.

 

I controlli [InkEdit](inkedit-control-reference.md) e [InkPicture](inkpicture-control-reference.md) possono essere usati per raccogliere input penna in Windows 2000 con Service Pack 4 o Windows XP Professional con Service Pack 2 quando i componenti della piattaforma Tablet PC sono presenti installando Tablet PC SDK versione 1.7, ma non sono in grado di raccogliere input penna in sistemi non Tablet PC in cui non sono installati i componenti della piattaforma Tablet PC.

L Windows SDK fornisce tutti i componenti necessari per sviluppare applicazioni Tablet PC in SKU non Tablet di Windows. Impostare la chiave **del Registro di sistema DWORD** seguente su 1 per raccogliere input penna su SKU non Tablet Windows:

`HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\TabletPC\Controls\EnableInkCollectionOnNonTablets`

Questa chiave è destinata solo allo sviluppo.

 

 



