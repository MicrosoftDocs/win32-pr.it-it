---
title: Image Mastering API
description: Image Mastering API
ms.assetid: 4902d3fb-3195-4909-ab64-28f8a77ba14c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e28f98422a1845234ec9eda7054978797c876a41a905484a95a505bdf4e133c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119611791"
---
# <a name="image-mastering-api"></a>Image Mastering API

## <a name="purpose"></a>Scopo

L'API microsoft Windows di masterizzazione delle immagini consente alle applicazioni di eseguire lo stageing e masterizzare le immagini su supporti di archiviazione ottici CD, DVD e Blu-ray. Questa API può essere utilizzata anche da altri supporti simili a dischi in cui le immagini sono disponibili nello stesso modo.

## <a name="developer-audience"></a>Sviluppatori

IMAPI è progettato per C/C++ e per Visual Basic sviluppatori e per coloro che scrivono script usando VBScript.

È consigliabile conoscere le tecnologie e i file system CD, DVD e Blu-ray. Gli sviluppatori possono trarre vantaggio da una familiarità con la revisione più recente di Multimedia Command (MMC) [in ftp://ftp.t10.org/t10/drafts/mmc6](https://www.microsoft.com/?ref=go).

## <a name="run-time-requirements"></a>Requisiti di runtime

IMAPI 2.0 è supportato in modo nativo a partire da Windows Vista e Windows Server 2008. L'abilitazione della funzionalità IMAPI 2.0 per Windows XP e Windows Server 2003 richiede l'installazione del pacchetto di aggiornamento [KB932716.](https://support.microsoft.com/kb/932716) Se questo pacchetto non è installato, Windows XP supporta ancora in modo nativo [IMAPI 1.0.](imapiv1.md)

> [!Note]  
> Il Windows Feature Pack per Archiviazione è disponibile al pubblico tramite [l'Area download Microsoft.](https://www.microsoft.com/downloads/details.aspx?FamilyID=63ab51ea-99c9-45c0-980a-c556746fcf05) Altre informazioni sulle modifiche specifiche [dell'API](what-s-new.md) sono disponibili nella sezione Novità.

 

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                             | Descrizione                                                                           |
|---------------------------------------------------|---------------------------------------------------------------------------------------|
| [Novità](what-s-new.md)<br/>           | Informazioni dettagliate su ogni versione significativa dell'API Image Mastering.<br/> |
| [Informazioni su IMAPI](about-imapi.md)<br/>         | Informazioni generali sull'API Image Mastering.<br/>                         |
| [Uso di IMAPI](using-imapi.md)<br/>         | Argomenti relativi alle attività che illustrano come usare l'API Image Mastering.<br/>   |
| [Informazioni di riferimento su IMAPI](imapi-reference.md)<br/> | Descrizioni dettagliate delle interfacce IMAPI e di altri elementi di programmazione.<br/>  |



 

## <a name="additional-resources"></a>Risorse aggiuntive

Altre informazioni su IMAPI e altri argomenti correlati sono disponibili nelle posizioni seguenti:



| Argomento                                                                                                 | Descrizione                                                                                                                                                                                                                                                                                                                                                                   |
|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Blog di Microsoft Optical Archiviazione](/archive/blogs/opticalstorage/)                | Vengono evidenziati argomenti incentrati sull'implementazione dell'API Image Mastering in scenari di sviluppo reali.                                                                                                                                                                                                                                                 |
| [Forum di discussione sulla piattaforma ottico](https://social.msdn.microsoft.com/forums/windowsopticalplatform/threads/)              | Discutere CDROM.SYS, IMAPIv2 e Live File System problemi. Questo forum è in particolare sugli argomenti a livello di sistema ed è destinato agli sviluppatori di applicazioni anziché agli utenti finali.                                                                                                                                                                                                 |
| [T10 Technical Committee](https://www.t10.org/)                       | Un comitato tecnico del Comitato internazionale per gli standard di tecnologia informatica (INCITS) ha pronunciato "informazioni dettagliate". INCITS è accreditato da e opera in base a regole approvate dal American National Standards Institute (ANSI). Queste regole sono progettate per garantire che gli standard volontari siano sviluppati dal consenso dei gruppi di settore. |
| [OSTA (Optical Archiviazione Technology Association)](http://www.osta.org/) | Si lavora per modellare il futuro del settore tramite riunioni regolari di Commercial Optical Archiviazione Applications (COSA), DVD Compatibility, Marketing, MPV (MusicPhotoVideo), dei comitato delle funzioni UDF e di un nuovo comitato adhoc Blue Meeting. Le aziende interessate in tutto il mondo sono invitate a partecipare all'organizzazione e a partecipare ai suoi comitato e programmi.               |



 

 

