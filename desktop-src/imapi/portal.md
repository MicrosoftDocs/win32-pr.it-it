---
title: API Di mastering delle immagini
description: API Di mastering delle immagini
ms.assetid: 4902d3fb-3195-4909-ab64-28f8a77ba14c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7fabf41d1c82420709b39bb5db03c2ac3e851d2
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119678"
---
# <a name="image-mastering-api"></a>API Di mastering delle immagini

## <a name="purpose"></a>Scopo

L'API di masterizzazione delle immagini di Microsoft Windows consente alle applicazioni di attivare e masterizzare le immagini su supporti di archiviazione ottica CD, DVD e Blu-ray. Anche altri supporti simili a dischi che denotano le immagini nello stesso modo possono usare questa API.

## <a name="developer-audience"></a>Sviluppatori

IMAPI è progettato per gli sviluppatori C/C++ e Visual Basic e per quelli che scrivono script usando VBScript.

È consigliabile conoscere le tecnologie e i file system cd, DVD e Blu-ray. Gli sviluppatori possono trarre vantaggio da una familiarità con la revisione più recente di Multimedia Command (MMC) [in ftp://ftp.t10.org/t10/drafts/mmc6](https://www.microsoft.com/?ref=go).

## <a name="run-time-requirements"></a>Requisiti di runtime

IMAPI 2.0 è supportato in modo nativo a partire da Windows Vista e Windows Server 2008. L'abilitazione della funzionalità IMAPI 2.0 per Windows XP e Windows Server 2003 richiede l'installazione del pacchetto di aggiornamento [KB932716.](https://support.microsoft.com/kb/932716) Se questo pacchetto non è installato, Windows XP supporta ancora in modo nativo [IMAPI 1.0.](imapiv1.md)

> [!Note]  
> Il Feature Pack di Windows per l'archiviazione è disponibile al pubblico tramite [l'Area download Microsoft.](https://www.microsoft.com/downloads/details.aspx?FamilyID=63ab51ea-99c9-45c0-980a-c556746fcf05) Altre informazioni sulle modifiche specifiche [dell'API](what-s-new.md) sono disponibili nella sezione Novità.

 

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                             | Descrizione                                                                           |
|---------------------------------------------------|---------------------------------------------------------------------------------------|
| [Novità](what-s-new.md)<br/>           | Informazioni dettagliate su ogni versione significativa dell'API Image Mastering.<br/> |
| [Informazioni su IMAPI](about-imapi.md)<br/>         | Informazioni generali sull'API Image Mastering.<br/>                         |
| [Uso di IMAPI](using-imapi.md)<br/>         | Argomenti correlati alle attività che illustrano come usare l'API Image Mastering.<br/>   |
| [Informazioni di riferimento su IMAPI](imapi-reference.md)<br/> | Descrizioni dettagliate delle interfacce IMAPI e di altri elementi di programmazione.<br/>  |



 

## <a name="additional-resources"></a>Risorse aggiuntive

Altre informazioni su IMAPI e altri argomenti correlati sono disponibili nelle posizioni seguenti:



| Argomento                                                                                                 | Descrizione                                                                                                                                                                                                                                                                                                                                                                   |
|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Microsoft Optical Storage Blog](/archive/blogs/opticalstorage/)                | Vengono evidenziati argomenti incentrati sull'implementazione dell'API Image Mastering negli scenari di sviluppo reali.                                                                                                                                                                                                                                                 |
| [Forum di discussione sulla piattaforma ottica](https://social.msdn.microsoft.com/forums/windowsopticalplatform/threads/)              | Illustrare CDROM.SYS, IMAPIv2 e Live File System problemi. Questo forum è in particolare sugli argomenti a livello di sistema ed è destinato agli sviluppatori di applicazioni anziché agli utenti finali.                                                                                                                                                                                                 |
| [Comitato tecnico T10](https://www.t10.org/)                       | Un comitato tecnico del comitato internazionale per gli standard di tecnologia dell'informazione (INCITS, pronunciato "insights"). INCITS è accreditato da e opera in base alle regole approvate da, American National Standards Institute (ANSI). Queste regole sono progettate per garantire che gli standard volontari siano sviluppati dal consenso dei gruppi di settore. |
| [OSTA (Optical Storage Technology Association)](http://www.osta.org/) | Funziona per modellare il futuro del settore tramite riunioni regolari di commercial optical storage applications (COSA), compatibilità DVD, marketing, MPV (MusicPhotoVideo), i comitato UDF e un nuovo comitato adhoc Blue Laser. Le aziende interessate in tutto il mondo sono invitate a unirsi all'organizzazione e a partecipare ai relativi programmi e commissioni.               |



 

 

