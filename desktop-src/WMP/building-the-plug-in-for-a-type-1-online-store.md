---
title: Creazione del plug-in per un negozio online di tipo 1
description: Creazione del plug-in per un negozio online di tipo 1
ms.assetid: 5d38a41f-9859-452b-953f-3449c2b0ce06
keywords:
- Windows Media Player Online Stores, plug-in
- archivi online, plug-in
- digitare 1 negozi online, plug-in
- Windows Media Player Online Stores, creazione di plug-in
- negozi online, compilazione di plug-in
- digitare 1 negozi online, compilazione di plug-in
- Windows Media Player Online Stores, interfaccia IWMPContentPartner
- negozi online, interfaccia IWMPContentPartner
- tipo 1 Store online, interfaccia IWMPContentPartner
- plug-in, archivi Windows Media Player online
- plug-in, archivi online
- plug-in, digitare 1 negozi online
- plug-in, interfaccia IWMPContentPartner
- plug-in, compilazione
- Plug-in di Windows Media Player, digitare 1 negozi online
- Plug-in di Windows Media Player, archivi online
- Plug-in di Windows Media Player, archivi Windows Media Player online
- Plug-in di Windows Media Player, interfaccia IWMPContentPartner
- Plug-in di Windows Media Player, compilazione
- IWMPContentPartner
- creazione di plug-in, digitare 1 Store online
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36272e3497eebc7b5362d793a0ee265d2c3166fc
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "106299439"
---
# <a name="building-the-plug-in-for-a-type-1-online-store"></a>Creazione del plug-in per un negozio online di tipo 1

Un archivio online di tipo 1 deve fornire un plug-in che implementi l'interfaccia [**IWMPContentPartner**](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner) . Il plug-in viene eseguito in un processo separato da Windows Media Player.

La procedura per la creazione di un plug-in che esegue out-of-process è la seguente:

1.  Scrivere il plug-in come se fosse un server COM in-process.
2.  Creare una voce del registro di sistema **DllSurrogate** nel computer dell'utente. La voce **DllSurrogate** informa il runtime COM che il plug-in deve essere creato in un'istanza del surrogato predefinito della DLL, dllhost.exe.

Per informazioni dettagliate sulla registrazione del plug-in, vedere [chiavi e voci del registro di sistema per un archivio online di tipo 1](registry-keys-and-entries-for-a-type-1-online-store.md).

Non è necessario creare codice proxy o stub per il plug-in. Tutto il supporto del marshalling viene fornito da Windows Media Player.

È possibile utilizzare la procedura guidata plug-in di Store online per creare rapidamente un plug-in che funge da punto di partenza. Per ulteriori informazioni, vedere [Installing the Online Store plug-in Wizard](installing-the-online-store-plug-in-wizard.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Guida per programmatori per i negozi di tipo 1 online**](programming-guide-for-type-1-online-stores.md)
</dt> </dl>

 

 




