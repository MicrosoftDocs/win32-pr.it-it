---
title: Negozi online esclusivi
description: Negozi online esclusivi
ms.assetid: f2b7f9a7-2299-48f4-b915-2c1a5e0d68bb
keywords:
- Windows Media Player Online Stores, esclusivo
- negozi online, esclusivi
- digitare 1 Store online, esclusivo
- digitare 2 archivi online, esclusivi
- negozi online esclusivi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f408a0ada0de46d637537ffccd3ec162da04e8ce
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "106299383"
---
# <a name="exclusive-online-stores"></a>Negozi online esclusivi

Con Windows Media Player 11, un'applicazione che incorpora il controllo Player in modalità remota può specificare un negozio online esclusivo. In tal caso, il selettore di servizio in Windows Media Player è disabilitato e solo l'archivio online specificato è disponibile per l'utente. Inoltre, Windows Media Player adotta il colore specificato dall'elemento **color** del documento ServiceInfo del negozio online esclusivo.

Per specificare un archivio online esclusivo, un'applicazione deve aggiungere ExclusiveService:*nome* -chiavi alla fine della stringa restituita da [IWMPRemoteMediaServices:: GetServiceType](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpremotemediaservices-getservicetype). Si supponga, ad esempio, che Proseware sia il nome della chiave assegnato a un particolare negozio online. Se **GetServiceType** restituisce la stringa "Remote ExclusiveService: proseware", Proseware sarà l'unico negozio online disponibile nel controllo lettore incorporato in remoto.

Un'applicazione può limitare il Media Player Windows a uno Store online esclusivo solo se Windows Media Player non è già in esecuzione quando viene avviata l'applicazione. È responsabilità dell'applicazione informare l'utente che deve chiudere Windows Media Player prima di eseguire l'applicazione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni comuni ai negozi online di tipo 1 e di tipo 2**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[**Gestione remota del controllo di Windows Media Player**](remoting-the-windows-media-player-control.md)
</dt> </dl>

 

 




