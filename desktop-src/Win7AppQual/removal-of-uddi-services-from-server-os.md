---
description: .
ms.assetid: 5ebc8c4c-acee-4658-8d36-30fbb17b1ef1
title: Rimozione dei servizi UDDI dal sistema operativo server
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7681167177b850ba44ac0fc26e019c7393008b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317618"
---
# <a name="removal-of-uddi-services-from-server-operating-system"></a>Rimozione dei servizi UDDI dal sistema operativo server

## <a name="affected-platform"></a>Piattaforma interessata

**Server** -Windows Server 2008 R2  



## <a name="feature-impact"></a>Effetto sulle funzionalità

**Gravità** -medio  
**Frequenza** -bassa  

## <a name="description"></a>Descrizione

Microsoft ha rimosso il ruolo del server Servizi UDDI (Universal Description, Discovery, and Integration) da Windows Server 2008 R2. Le versioni future dei servizi UDDI faranno parte del prodotto Microsoft BizTalk. Il riallineamento e il consolidamento del prodotto consentono a Microsoft di gestire al meglio il mercato SOA (Service-Oriented Architecture).

La prima versione Post-Windows Server 2008 dei servizi UDDI sarà conforme agli standard UDDI v 3.0. Verrà fornito come parte della versione di BizTalk Server 2009. Per soddisfare il nostro impegno a offrire un'esperienza utente soddisfacente, offriamo un pacchetto di installazione di servizi UDDI V3 per Windows Server 2008 R2.

## <a name="manifestation"></a>Manifestazione

La presenza di versioni precedenti dei componenti dei servizi UDDI nel sistema blocca l'aggiornamento a Windows Server 2008 R2.

## <a name="mitigation-of-impact"></a>Attenuazione dell'effetto

Gli utenti che hanno distribuito un sito di servizi UDDI da Windows Server 2003 o Windows Server 2008 possono scegliere di non aggiornare i server che eseguono i servizi UDDI a Windows Server 2008 R2. Possono inoltre spostare i servizi UDDI in caselle dedicate di Windows Server 2003 o Windows Server 2008 se è necessario aggiornare le caselle attuali dei servizi UDDI.

## <a name="solution"></a>Soluzione

La soluzione consigliata consiste nel distribuire i servizi UDDI v 3.0 da BizTalk Server 2009 in un computer Windows Server 2008 R2 e quindi eseguire la migrazione del sito precedente al nuovo sito. UDDI Services v 3.0 fornisce la compatibilità con le versioni precedenti dei servizi UDDI 2,0, pertanto tutte le applicazioni che utilizzano servizi UDDI non saranno interessate.

A questo scopo, seguire questa procedura:

1.  Configurare un nuovo sito dei servizi UDDI v 3.0 in un computer già caricato con Windows Server 2008 R2. Nota: in una configurazione distribuita, un sito UDDI v 3.0 può essere costituito da più di un computer Windows Server 2008 R2.
2.  Utilizzare l'utilità di migrazione dati UDDI per eseguire la migrazione dei dati dal database dei servizi UDDI precedente al nuovo database.
3.  Eseguire il backup del database dei servizi UDDI precedente per garantire la funzionalità di rollback.
4.  Disinstallare il software dei servizi UDDI precedente, quindi aggiornare le caselle a Windows Server 2008 R2.

## <a name="links-to-other-resources"></a>Collegamenti ad altre risorse

-   [Sito Web dei servizi UDDI Microsoft](https://msdn.microsoft.com/biztalk/dd789428.aspx)
-   [Specifiche UDDI](http://uddi.xml.org/specification)
-   [Download di servizi UDDI v 3.0 per Windows Server 2008 R2](https://www.microsoft.com/downloads/details.aspx?FamilyID=e4761835-70f0-4e8d-96c5-64818d54e06e)

 

 



