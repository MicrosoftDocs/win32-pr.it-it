---
title: Microsoft Interface Definition Language
description: Il Microsoft Interface Definition Language (MIDL) definisce le interfacce tra i programmi client e server.
ms.assetid: 5ed1ff94-bbcb-4c6e-83aa-63d24eb84859
keywords:
- MIDL MIDL
- MIDL MIDL (vedere Microsoft Interface Definition Language MIDL)
- Microsoft Interface Definition Language MIDL
- Microsoft Interface Definition Language MIDL, pagina iniziale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e274d66ae234205f5db1f41b2d191ea409561bd
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104046641"
---
# <a name="microsoft-interface-definition-language"></a>Microsoft Interface Definition Language

## <a name="purpose"></a>Scopo

Il Microsoft Interface Definition Language (MIDL) definisce le interfacce tra i programmi client e server. Microsoft include il compilatore MIDL con Platform Software Development Kit (SDK) per consentire agli sviluppatori di creare i file IDL (Interface Definition Language) e i file di configurazione dell'applicazione (ACF) necessari per le interfacce RPC (Remote Procedure Call) e le interfacce COM/DCOM. MIDL supporta inoltre la generazione di librerie dei tipi per l'automazione OLE.

## <a name="where-applicable"></a>Se applicabile

MIDL può essere usato in tutte le applicazioni client/server basate su sistemi operativi Windows. Può essere usato anche per creare programmi client e server per ambienti di rete eterogenei che includono sistemi operativi come UNIX e Apple. Microsoft supporta il gruppo aperto (noto in precedenza come Open Software Foundation) DCE standard per l'interoperabilità RPC.

## <a name="developer-audience"></a>Sviluppatori

Quando si usa MIDL con RPC, è necessaria una certa familiarità con la programmazione C/C++ e il paradigma RPC. Quando si usa MIDL con COM, è necessaria una certa familiarità con la programmazione C++ e il paradigma RPC che si applica a COM. in alternativa, è necessaria una certa familiarità con gli script e le librerie dei tipi di modelli di automazione OLE.

## <a name="run-time-requirements"></a>Requisiti di runtime

Le librerie di runtime appropriate per l'utilizzo di MIDL sono incluse in Windows. Il compilatore MIDL e i componenti dell'ambiente di sviluppo RPC vengono installati quando si installa il Windows SDK. Per ulteriori informazioni, vedere [utilizzo del compilatore MIDL](using-the-midl-compiler-2.md) e [installazione dell'ambiente di programmazione RPC](/windows/desktop/Rpc/installing-the-rpc-programming-environment).

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                               | Descrizione                                                                        |
|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [Overview](about-this-guide-2.md)<br/>                                                       | Informazioni generali su MIDL e sul compilatore MIDL.<br/>                   |
| [Uso del compilatore MIDL](using-the-midl-compiler-2.md)<br/>                                 | Informazioni sull'uso di MIDL compilatore per generare stub RPC.<br/>       |
| [Definizioni di interfaccia e librerie dei tipi](interface-definitions-and-type-libraries.md)<br/> | Documentazione delle definizioni di interfaccia specifiche di RPC e delle librerie dei tipi.<br/> |
| [Riferimento Command-Line MIDL](midl-command-line-reference.md)<br/>                           | Documentazione delle opzioni della riga di comando del compilatore MIDL.<br/>               |
| [Riferimenti per il linguaggio MIDL](midl-language-reference.md)<br/>                                   | Riferimenti al linguaggio del compilatore MIDL.<br/>                                   |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[RPC (Remote Procedure Call)](/windows/desktop/Rpc/rpc-start-page)
</dt> </dl>

 

