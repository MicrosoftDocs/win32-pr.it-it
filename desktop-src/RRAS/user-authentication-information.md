---
title: Informazioni di autenticazione utente
description: Il servizio gestione connessione di accesso remoto nel computer client invia un nome utente e una password al server RAS nel computer remoto.
ms.assetid: b27bf520-d871-4314-8ed9-3a6a9583ab52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0cb95d0e941c47deb398c03277013e0e0a35f9d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103872594"
---
# <a name="user-authentication-information"></a>Informazioni di autenticazione utente

Il servizio gestione connessione di accesso remoto nel computer client invia un nome utente e una password al server RAS nel computer remoto. Prima di stabilire una connessione, il server remoto utilizza queste informazioni per autenticare l'utente. Per impostazione predefinita, la gestione connessione di accesso remoto invia il nome utente e la password dell'utente attualmente connesso. Il client RAS può utilizzare la struttura [**RASDIALPARAMS**](/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)) specificata nella chiamata [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) per specificare un nome utente e una password diversi.

Se il server remoto non è in grado di autenticare l'utente con le informazioni specificate, può consentire all'operazione di connessione di entrare in uno [stato di sospensione](paused-states.md) per consentire al client RAS di raccogliere dati di autenticazione diversi dall'utente.

 

 