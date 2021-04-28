---
description: Rimozione di Servizi UDDI dal sistema operativo del server
ms.assetid: 5ebc8c4c-acee-4658-8d36-30fbb17b1ef1
title: Rimozione di Servizi UDDI dal sistema operativo del server
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 960a4063d990a3b2cdac45cd933a1e7dfef41f88
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116329"
---
# <a name="removal-of-uddi-services-from-server-operating-system"></a>Rimozione di Servizi UDDI dal sistema operativo del server

## <a name="affected-platform"></a>Piattaforma interessata

**Server** - Windows Server 2008 R2  



## <a name="feature-impact"></a>Impatto sulle funzionalità

**Gravità** - Media  
**Frequenza** - Bassa  

## <a name="description"></a>Descrizione

Microsoft ha rimosso il ruolo del server Servizi UDDI (Universal Description, Discovery, and Integration) da Windows Server 2008 R2. Le versioni future di Servizi UDDI saranno parte del prodotto Microsoft BizTalk. Questo riallineamento e consolidamento del prodotto posiziona Microsoft per gestire meglio il mercato dell'architettura orientata ai servizi (SOA).

La prima versione successiva a Windows Server 2008 di Servizi UDDI sarà conforme agli standard UDDI v3.0. Verrà rilasciato come parte della versione BizTalk Server 2009. Per soddisfare il nostro impegno a offrire un'esperienza utente soddisfacente, verrà offerto un pacchetto di installazione di Servizi UDDI v3 per Windows Server 2008 R2.

## <a name="manifestation"></a>Manifestazione

La presenza di versioni precedenti dei componenti di Servizi UDDI nel sistema blocca un aggiornamento a Windows Server 2008 R2.

## <a name="mitigation-of-impact"></a>Mitigazione dell'impatto

Gli utenti che hanno distribuito un sito di Servizi UDDI da Windows Server 2003 o Windows Server 2008 possono scegliere di non aggiornare i server che eseguono i servizi UDDI a Windows Server 2008 R2. Possono anche spostare i servizi UDDI in caselle dedicate di Windows Server 2003 o Windows Server 2008 se è necessario aggiornare le caselle di Servizi UDDI correnti.

## <a name="solution"></a>Soluzione

La soluzione consigliata consiste nel distribuire Servizi UDDI v3.0 da BizTalk Server 2009 in un computer Windows Server 2008 R2 e quindi eseguire la migrazione del sito precedente al nuovo sito. Servizi UDDI v3.0 garantisce la compatibilità con le versioni precedenti di Servizi UDDI 2.0, pertanto tutte le applicazioni che usano Servizi UDDI non saranno interessate.

A questo scopo, seguire questa procedura:

1.  Configurare un nuovo sito di Servizi UDDI v3.0 in un computer già caricato con Windows Server 2008 R2. Nota: in un'installazione distribuita un sito UDDI v3.0 può essere costituito da più computer Windows Server 2008 R2.
2.  Usare lo strumento di migrazione dei dati UDDI per eseguire la migrazione dei dati dal database di Servizi UDDI precedente al nuovo database.
3.  Eseguire il backup del database di Servizi UDDI precedente per garantire la funzionalità di rollback.
4.  Disinstallare il software di Servizi UDDI precedente e quindi aggiornare tali caselle a Windows Server 2008 R2.

## <a name="links-to-other-resources"></a>Collegamenti ad altre risorse

-   [Sito Web di Servizi UDDI Microsoft](https://msdn.microsoft.com/biztalk/dd789428.aspx)
-   [Specifiche UDDI](http://uddi.xml.org/specification)
-   [Download di Servizi UDDI v3.0 per Windows Server 2008 R2](https://www.microsoft.com/downloads/details.aspx?FamilyID=e4761835-70f0-4e8d-96c5-64818d54e06e)

 

 



