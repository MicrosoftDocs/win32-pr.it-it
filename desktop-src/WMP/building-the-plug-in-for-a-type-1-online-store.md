---
title: Compilazione del plug-in per uno Store online di tipo 1
description: Compilazione del plug-in per uno Store online di tipo 1
ms.assetid: 5d38a41f-9859-452b-953f-3449c2b0ce06
keywords:
- Windows Media Player negozi online, plug-in
- negozi online, plug-in
- tipo 1 negozi online, plug-in
- Windows Media Player negozi online, creazione di plug-in
- negozi online, creazione di plug-in
- tipo 1 negozi online, creazione di plug-in
- Windows Media Player store online, interfaccia IWMPContentPartner
- negozi online, interfaccia IWMPContentPartner
- Tipo 1 negozi online, interfaccia IWMPContentPartner
- plug-in, Windows Media Player online store
- plug-in, negozi online
- plug-in, tipo 1 negozi online
- plug-in, interfaccia IWMPContentPartner
- plug-in, compilazione
- Windows Media Player plug-in, tipo 1 negozi online
- Windows Media Player plug-in, negozi online
- Windows Media Player plug-in, Windows Media Player online store
- Windows Media Player plug-in, interfaccia IWMPContentPartner
- Windows Media Player plug-in, compilazione
- IWMPContentPartner
- creazione di plug-in, tipo 1 negozi online
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1fdc5b01a0a8ec526af22e6be90c562524536cdb30b37bd03eb40132af0be49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118997851"
---
# <a name="building-the-plug-in-for-a-type-1-online-store"></a>Compilazione del plug-in per uno Store online di tipo 1

Un negozio online di tipo 1 deve fornire un plug-in che implementa [**l'interfaccia IWMPContentPartner.**](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner) Il plug-in viene eseguito in un processo separato da Windows Media Player.

I passaggi per la creazione di un plug-in che viene eseguito out-of-process sono i seguenti:

1.  Scrivere il plug-in come se fosse un server COM in-process.
2.  Creare una voce del Registro di sistema **DllSurrogate** nel computer dell'utente. La **voce DllSurrogate** informa il runtime COM che il plug-in deve essere creato in un'istanza del surrogato DLL predefinito, dllhost.exe.

Per informazioni dettagliate sulla registrazione del plug-in, vedere Chiavi e voci del Registro di sistema per un Negozio [online di tipo 1.](registry-keys-and-entries-for-a-type-1-online-store.md)

Non è necessario creare codice proxy o stub per il plug-in. Tutto il supporto per il marshalling viene fornito da Windows Media Player.

È possibile usare la procedura guidata plug-in del negozio online per creare rapidamente un plug-in che funge da punto di partenza. Per altre informazioni, vedere [Installazione guidata plug-in](installing-the-online-store-plug-in-wizard.md)di Online Store.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Guida per programmatori per i negozi online di tipo 1**](programming-guide-for-type-1-online-stores.md)
</dt> </dl>

 

 




