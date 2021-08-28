---
title: Informazioni di autenticazione utente
description: Il servizio di Gestione connessioni remoto nel computer client invia un nome utente e una password al server RAS nel computer remoto.
ms.assetid: b27bf520-d871-4314-8ed9-3a6a9583ab52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f347cd9f42106619f2558bdcbc677c961b4fae749912c92dd32ac2c8096f6fd7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127811"
---
# <a name="user-authentication-information"></a>Informazioni di autenticazione utente

Il servizio di Gestione connessioni remoto nel computer client invia un nome utente e una password al server RAS nel computer remoto. Prima di stabilire una connessione, il server remoto usa queste informazioni per autenticare l'utente. Per impostazione predefinita, il Gestione connessioni remoto invia il nome utente e la password dell'utente attualmente connesso. Il client RAS può usare la [**struttura RASDIALPARAMS**](/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)) specificata nella [**chiamata RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) per specificare un nome utente e una password diversi.

Se il server remoto non è in grado di autenticare l'utente con le informazioni specificate, può consentire all'operazione di connessione di entrare [in](paused-states.md) uno stato sospeso per consentire al client RAS di raccogliere dati di autenticazione diversi dall'utente.

 

 