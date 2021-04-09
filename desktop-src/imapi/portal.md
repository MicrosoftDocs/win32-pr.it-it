---
title: API per la creazione di immagini master
description: .
ms.assetid: 4902d3fb-3195-4909-ab64-28f8a77ba14c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc23c972cf111dee5edf3cb014a52351eda3605e
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/09/2020
ms.locfileid: "103963536"
---
# <a name="image-mastering-api"></a>API per la creazione di immagini master

## <a name="purpose"></a>Scopo

L'API per la gestione delle immagini di Microsoft Windows consente alle applicazioni di organizzare e masterizzare immagini in supporti di archiviazione ottica CD, DVD e blu-ray. Anche altri supporti di tipo disco che dispongono di immagini nello stesso modo possono usare questa API.

## <a name="developer-audience"></a>Sviluppatori

IMAPi è progettato per C/C++ e Visual Basic gli sviluppatori e per quelli che scrivono script che usano VBScript.

È consigliabile conoscere le tecnologie CD, DVD e blu-ray e i file System. Gli sviluppatori possono trarre vantaggio da una certa familiarità con la revisione più recente del comando multimediale (MMC) in [FTP://FTP.T10.org/T10/Drafts/MMC6](https://www.microsoft.com/?ref=go).

## <a name="run-time-requirements"></a>Requisiti di runtime

IMAPi 2,0 è supportato a livello nativo a partire da Windows Vista e Windows Server 2008. Per abilitare la funzionalità IMAPi 2,0 per Windows XP e Windows Server 2003, è necessario installare il pacchetto di aggiornamento [KB932716](https://support.microsoft.com/kb/932716) . Se il pacchetto non è installato, Windows XP supporta ancora in modo nativo [imapi 1,0](imapiv1.md).

> [!Note]  
> Il Feature Pack di Windows per l'archiviazione è disponibile per il pubblico tramite l' [area download Microsoft](https://www.microsoft.com/downloads/details.aspx?FamilyID=63ab51ea-99c9-45c0-980a-c556746fcf05). Ulteriori informazioni relative alle modifiche specifiche dell'API sono disponibili nella sezione [novità](what-s-new.md) .

 

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                             | Descrizione                                                                           |
|---------------------------------------------------|---------------------------------------------------------------------------------------|
| [Novità](what-s-new.md)<br/>           | Informazioni che descrivono in dettaglio ogni versione significativa dell'API per la creazione di immagini master.<br/> |
| [Informazioni su IMAPi](about-imapi.md)<br/>         | Informazioni generali sull'API per la creazione di immagini master.<br/>                         |
| [Uso di IMAPi](using-imapi.md)<br/>         | Argomenti correlati alle attività che illustrano come usare l'API per la creazione di immagini master.<br/>   |
| [Riferimento a IMAPi](imapi-reference.md)<br/> | Descrizioni dettagliate delle interfacce IMAPi e altri elementi di programmazione.<br/>  |



 

## <a name="additional-resources"></a>Risorse aggiuntive

Altre informazioni su IMAPi e altri argomenti correlati sono disponibili nelle posizioni seguenti:



|                                                                                                  |                                                                                                                                                                                                                                                                                                                                                                    |
|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Blog di Microsoft Optical Storage](/archive/blogs/opticalstorage/)                | Mette in evidenza gli argomenti che si concentrano sull'implementazione dell'API Master immagini negli scenari di sviluppo reali.                                                                                                                                                                                                                                                 |
| [Forum di discussione sulla piattaforma ottica](https://social.msdn.microsoft.com/forums/windowsopticalplatform/threads/)              | Esaminare CDROM.SYS, IMAPIv2 e i problemi del file System Live. Questo forum è incentrato sugli argomenti a livello di sistema ed è destinato agli sviluppatori di applicazioni invece che agli sviluppatori.                                                                                                                                                                                                 |
| [Comitato tecnico T10](https://www.t10.org/)                       | Un comitato tecnico del Comitato internazionale per gli standard Information Technology (INCIs), pronunciato "Insights". Gli INCI sono accreditati da e operano con regole approvate da, il American National Standards Institute (ANSI). Queste regole sono progettate per garantire che gli standard volontari siano sviluppati dal consenso dei gruppi di settore. |
| [Associazione di tecnologie di archiviazione ottica (OSTA)](http://www.osta.org/) | Funziona per definire il futuro del settore attraverso riunioni regolari di applicazioni di archiviazione ottica (COSA), compatibilità dei DVD, marketing, MPV (MusicPhotoVideo), comitati UDF e un nuovo comitato di laser Blue ad hoc. Le aziende interessate in tutto il mondo sono invitati a partecipare all'organizzazione e a partecipare ai suoi comitati e programmi.               |



 

 

