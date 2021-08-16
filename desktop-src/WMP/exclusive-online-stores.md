---
title: Negozi online esclusivi
description: Negozi online esclusivi
ms.assetid: f2b7f9a7-2299-48f4-b915-2c1a5e0d68bb
keywords:
- Windows Media Player online store, exclusive
- negozi online, esclusivo
- store online di tipo 1, esclusivo
- Store online di tipo 2, esclusivo
- negozi online esclusivi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d199c47a201743ca56f9f9f199b5202bbdbe5fb320628afc5052b0ca8b969c24
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119650091"
---
# <a name="exclusive-online-stores"></a>Negozi online esclusivi

Con Windows Media Player 11, un'applicazione che incorpora il controllo Player in modalità remota può specificare un negozio online esclusivo. In tal caso, il selettore del servizio Windows Media Player è disabilitato e solo il negozio online specificato è disponibile per l'utente. Inoltre, Windows Media Player adotta il colore specificato dall'elemento **Color** del documento ServiceInfo del negozio online esclusivo.

Per specificare un negozio online esclusivo, un'applicazione deve aggiungere ExclusiveService:*keyname* alla fine della stringa restituita da [IWMPRemoteMediaServices::GetServiceType](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpremotemediaservices-getservicetype). Si supponga, ad esempio, che Proseware sia il nome della chiave assegnato a un particolare negozio online. Se **GetServiceType** restituisce la stringa "Remote ExclusiveService:Proseware", Proseware sarà l'unico negozio online disponibile nel controllo Player incorporato in remoto.

Un'applicazione può Windows Media Player a un negozio online esclusivo solo se Windows Media Player non è già in esecuzione all'avvio dell'applicazione. È responsabilità dell'applicazione informare l'utente che deve chiudere il Windows Media Player prima di eseguire l'applicazione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni comuni ai negozi online di tipo 1 e 2**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[**Gestione remota del controllo di Windows Media Player**](remoting-the-windows-media-player-control.md)
</dt> </dl>

 

 




