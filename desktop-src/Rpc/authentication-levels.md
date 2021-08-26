---
title: Livelli di autenticazione
description: Microsoft RPC fornisce più livelli di autenticazione.
ms.assetid: d9ed938e-4cd4-4355-8d08-830f955dd00c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cff12dae7331577da7748c2dc069bd6e7e4af6cfb1961f80d3de461930ddc3e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120080901"
---
# <a name="authentication-levels"></a>Livelli di autenticazione

Microsoft RPC fornisce più livelli di autenticazione. A seconda del livello di autenticazione, l'origine del traffico (quale entità di sicurezza ha inviato il traffico) può essere verificata quando viene stabilita la connessione, quando il client avvia una nuova chiamata di procedura remota o durante ogni scambio di pacchetti tra il client e il server.

Anche quando il mittente del traffico viene verificato, la sicurezza è ancora debole, poiché tale verifica non garantisce che il pacchetto non sia stato modificato o danneggiato durante il routing. verifica solo che il pacchetto provenisca dall'entità specificata. Per una maggiore sicurezza, le applicazioni distribuite possono impostare la libreria di runtime RPC per verificare che nessuno dei dati s scambiati tra il client e il server sia stato modificato. La libreria RPC può anche crittografare il contenuto di ogni pacchetto prima di inviarlo. In generale, le applicazioni che vogliono proteggere il traffico devono usare solo gli ultimi due livelli: integrità e privacy.

Tenere presente che livelli più elevati di autenticazione richiedono un sovraccarico di calcolo superiore. Lo sviluppatore deve decidere quale è più importante per l'applicazione, ovvero velocità o sicurezza. La maggior parte degli sviluppatori trova che con alcuni test delle prestazioni possono ottenere livelli di prestazioni accettabili mantenendo una sicurezza adeguata.

Le parti client e server dell'applicazione distribuita devono usare lo stesso livello di autenticazione. Per un elenco dei livelli di autenticazione RPC, vedere [Costanti a livello di autenticazione](authentication-level-constants.md).

 

 




