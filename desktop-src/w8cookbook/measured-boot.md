---
title: Avvio con misurazioni
description: Avvio con misurazioni
ms.assetid: D7ED02FA-6D0F-4753-AC07-BD7DCE55B3FD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d728a1980bc9a461e6383b1dea2bd7eb4aab461
ms.sourcegitcommit: f14de4414da072d5a761e946aedfde24d8b65102
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/30/2021
ms.locfileid: "108314342"
---
# <a name="measured-boot"></a>Avvio con misurazioni

## <a name="platforms"></a>Piattaforme

 **Client** - Windows 8  
**Server** - Windows Server 2012  



## <a name="description"></a>Descrizione

Poiché il software antimalware (AM) è diventato sempre più in grado di rilevare malware di runtime, anche gli utenti malintenzionati stanno diventando più esperti nella creazione di rootkit che possono nascondersi dal rilevamento. Il rilevamento di malware che inizia all'inizio del ciclo di avvio è una sfida che la maggior parte dei fornitori am affronta con attenzione. In genere, creano attacchi di sistema che non sono supportati dal sistema operativo host e possono effettivamente comportare il posizionamento del computer in uno stato instabile. Fino a questo punto, Windows non ha fornito un modo efficace per am per rilevare e risolvere queste minacce di avvio anticipato. Windows 8 introduce una nuova funzionalità denominata avvio con misurazioni, che misura ogni componente, dal firmware verso l'alto fino ai driver di avvio, archivia tali misurazioni nel Trusted Platform Module (TPM) nel computer e quindi rende disponibile un log che può essere testato in remoto per verificare lo stato di avvio del client.

## <a name="manifestation"></a>Manifestazione

La avvio con misurazioni offre al software AM un log attendibile (resistente allo spoofing e alla manomissione) di tutti i componenti di avvio avviati prima del software AM. Il software AM può usare il log per determinare se i componenti evasi prima di esso sono attendibili o se sono infetti da malware. Il software AM nel computer locale può inviare il log a un server remoto per la valutazione. Il server remoto può avviare azioni di correzione interagendo con il software nel client o tramite meccanismi fuori banda, a seconda dei casi.

## <a name="mitigation"></a>Mitigazione

Negli scenari aziendali, l'amministratore di sistema ha il controllo avvio con misurazioni vengono usate le informazioni. Negli scenari degli utenti finali, ad esempio nel settore bancario online, il consumer deve acconsentire esplicitamente all'uso avvio con misurazioni per il servizio specifico.

## <a name="solution"></a>Soluzione

È white paper in corso una preparazione che dettagli le API e le chiamate di funzione che devono essere effettuate per vari avvio con misurazioni scenari.

 

 




