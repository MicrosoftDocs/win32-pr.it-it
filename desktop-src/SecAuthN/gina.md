---
description: Lo scopo di una DLL GINA è fornire procedure di identificazione utente e autenticazione personalizzabili. L'impostazione predefinita DIA esegue questa operazione delegando il monitoraggio degli eventi di firma di accesso condiviso a Winlogon, che riceve ed elabora sequenze di attenzione sicura CTL+ALT+DEL.
ms.assetid: 035e9c8b-2490-438d-8f02-7e0f039f960f
title: Gina
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5dad8917a24100fbf5c6c36eab3bbfc5b67baf62b378f9207626378fe864b672
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119623141"
---
# <a name="gina"></a>Gina

GINA opera nel [*contesto*](/windows/desktop/SecGloss/c-gly) del processo [*Winlogon*](/windows/desktop/SecGloss/w-gly) e, di conseguenza, la DLL [*GINA*](/windows/desktop/SecGloss/g-gly) viene caricata molto presto nel processo di avvio. La DLL GINA deve seguire le regole in modo che l'integrità del sistema sia mantenuta, in particolare per quanto riguarda l'interazione con l'utente.

> [!Note]  
> Le DLL GINA vengono ignorate in Windows Vista.

 

L'uso più comune di GINA è la comunicazione con un dispositivo esterno, ad esempio un lettore di smart [*card.*](/windows/desktop/SecGloss/r-gly) È essenziale impostare il parametro start per il driver di dispositivo sul sistema (Winnt.h: SERVICE SYSTEM START) per assicurarsi che il driver sia caricato al momento della chiamata di \_ \_ GINA.

Lo scopo di una DLL GINA è fornire procedure di identificazione utente e autenticazione personalizzabili. L'impostazione predefinita DIA esegue questa operazione delegando il monitoraggio degli eventi di firma [](/windows/desktop/SecGloss/s-gly) di accesso condiviso a Winlogon, che riceve ed elabora sequenze di attenzione sicura CTL+ALT+DEL. Un'istanza DIA personalizzata è responsabile della configurazione per la ricezione di eventi di firma di accesso condiviso (diversi dall'evento di firma di accesso condiviso predefinito CTRL+ALT+CANC) e della notifica a Winlogon quando si verificano eventi di firma di accesso condiviso. Winlogon ne valuterà lo stato per determinare ciò che è necessario per elaborare la firma di accesso condiviso di GINA personalizzata. Questa elaborazione include in genere chiamate alle funzioni di elaborazione SAS di GINA.

Per informazioni sulle funzioni di esportazione GINA specifiche, vedere [FUNZIONI DI ESPORTAZIONE DI GINA](authentication-functions.md). Per informazioni sull'uso delle strutture GINA per passare informazioni, vedere [Strutture GINA](authentication-structures.md).



| Argomento                                                                             | Descrizione                                                                     |
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [Caricamento ed esecuzione di una DLL GINA](loading-and-running-a-gina-dll.md)<br/>   | Valore della chiave del Registro di sistema da modificare per caricare ed eseguire una DLL GINA personalizzata.<br/> |
| [Compilazione e test di una DLL GINA](building-and-testing-a-gina-dll.md)<br/> | Come testare una DLL GINA.<br/>                                              |



 

 

