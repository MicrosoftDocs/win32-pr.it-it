---
title: Avvio con misurazioni
description: Avvio con misurazioni
ms.assetid: D7ED02FA-6D0F-4753-AC07-BD7DCE55B3FD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ccbba6e5f96fd91c00c295c4b15cab8849f11dc
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/01/2020
ms.locfileid: "103730738"
---
# <a name="measured-boot"></a>Avvio con misurazioni

## <a name="platforms"></a>Piattaforme

 **Client** -Windows 8  
**Server** -Windows Server 2012  



## <a name="description"></a>Descrizione

Poiché il software antimalware (AM) è diventato migliore e migliore nel rilevamento del malware di runtime, anche gli utenti malintenzionati stanno migliorando la creazione di rootkit che possono nascondere il rilevamento. Il rilevamento di malware che inizia nelle prime fasi del ciclo di avvio è una sfida che la maggior parte dei fornitori di AM deve affrontare diligentemente. In genere, creano hack di sistema non supportati dal sistema operativo host e possono effettivamente comportare il posizionamento del computer in uno stato instabile. Fino a questo punto, Windows non ha fornito un metodo efficace per rilevare e risolvere queste minacce iniziali di avvio. In Windows 8 è stata introdotta una nuova funzionalità denominata avvio misurato, che misura ogni componente, dal firmware fino ai driver di avvio, archivia tali misure nel Trusted Platform Module (TPM) nel computer e quindi rende disponibile un log che può essere testato in remoto per verificare lo stato di avvio del client.

## <a name="manifestation"></a>Manifestazione

La funzionalità di avvio misurato fornisce il software AM con un registro attendibile (resistente a spoofing e manomissioni) di tutti i componenti di avvio avviati prima del software AM. Il software AM può utilizzare il log per determinare se i componenti eseguiti prima di essere attendibili o se sono infetti da malware. Il software AM nel computer locale può inviare il log a un server remoto per la valutazione. Il server remoto può avviare azioni correttive interagendo con il software sul client o tramite meccanismi fuori banda, a seconda dei casi.

## <a name="mitigation"></a>Strategia di riduzione del rischio

Negli scenari aziendali, l'amministratore di sistema ha il controllo del modo in cui vengono usate le informazioni di avvio misurate. Negli scenari dell'utente finale, ad esempio il servizio online banking, il consumer deve acconsentire esplicitamente all'uso dell'avvio misurato per il servizio specifico.

## <a name="solution"></a>Soluzione

Viene preparata una white paper che descrive in dettaglio le API e le chiamate di funzione che devono essere eseguite per diversi scenari di avvio misurato.

 

 




