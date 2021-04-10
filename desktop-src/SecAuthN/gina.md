---
description: Lo scopo di una DLL GINA è fornire procedure di identificazione e autenticazione utente personalizzabili. Per impostazione predefinita, GINA esegue questa operazione delegando il monitoraggio degli eventi SAS a Winlogon, che riceve ed elabora le sequenze di attenzione (SASs, Secure Attention Sequence) CTL + ALT + CANC.
ms.assetid: 035e9c8b-2490-438d-8f02-7e0f039f960f
title: GINA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 084a65ad42bdbe030e697481501a4dc60e54baef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758267"
---
# <a name="gina"></a>GINA

[*Gina*](/windows/desktop/SecGloss/g-gly) opera nel [*contesto*](/windows/desktop/SecGloss/c-gly) del processo [*Winlogon*](/windows/desktop/SecGloss/w-gly) e, di conseguenza, la DLL GINA viene caricata molto presto nel processo di avvio. La DLL GINA deve seguire le regole in modo che l'integrità del sistema venga mantenuta, in particolare in relazione all'interazione con l'utente.

> [!Note]  
> Le DLL GINA vengono ignorate in Windows Vista.

 

L'uso più comune di GINA consiste nel comunicare con un dispositivo esterno, ad esempio un [*lettore*](/windows/desktop/SecGloss/r-gly)di smart card. È essenziale impostare il parametro Start per il driver di dispositivo su System (Winnt. h: SERVICE \_ System \_ Start) per assicurarsi che il driver venga caricato nel momento in cui Gina viene richiamato.

Lo scopo di una DLL GINA è fornire procedure di identificazione e autenticazione utente personalizzabili. Per impostazione predefinita, GINA esegue questa operazione delegando il monitoraggio degli eventi SAS a Winlogon, che riceve ed elabora le sequenze di attenzione (SASs, [*Secure Attention Sequence*](/windows/desktop/SecGloss/s-gly) ) CTL + ALT + CANC. Un oggetto GINA personalizzato è responsabile dell'impostazione per la ricezione di eventi di firma di accesso condiviso (ad eccezione dell'evento di firma di accesso condiviso con CTRL + ALT + CANC) e la notifica di Winlogon quando si verificano eventi SAS. Winlogon valuterà il proprio stato per determinare gli elementi necessari per elaborare la firma di accesso condiviso di GINA personalizzata. Questa elaborazione include in genere le chiamate alle funzioni di elaborazione SAS di GINA.

Per informazioni sulle funzioni di esportazione GINA specifiche, vedere [funzioni di esportazione Gina](authentication-functions.md). Per informazioni sull'utilizzo delle strutture GINA per il passaggio di informazioni, vedere la pagina relativa alle [strutture Gina](authentication-structures.md).



| Argomento                                                                             | Descrizione                                                                     |
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [Caricamento ed esecuzione di una DLL GINA](loading-and-running-a-gina-dll.md)<br/>   | Il valore della chiave del registro di sistema da modificare per caricare ed eseguire una DLL GINA personalizzata.<br/> |
| [Compilazione e test di una DLL GINA](building-and-testing-a-gina-dll.md)<br/> | Come testare una DLL GINA.<br/>                                              |



 

 

