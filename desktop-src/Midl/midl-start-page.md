---
title: Microsoft Interface Definition Language
description: Il Microsoft Interface Definition Language (MIDL) definisce le interfacce tra i programmi client e server.
ms.assetid: 5ed1ff94-bbcb-4c6e-83aa-63d24eb84859
keywords:
- MIDL MIDL
- MIDL MIDL ( Vedere Microsoft Interface Definition Language MIDL )
- Microsoft Interface Definition Language MIDL
- Microsoft Interface Definition Language MIDL , pagina iniziale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9062d5b2af18f7c3aa5ad57a4cb8f606cccc43333e4eff17d3518f72b7a064a4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119534971"
---
# <a name="microsoft-interface-definition-language"></a>Microsoft Interface Definition Language

## <a name="purpose"></a>Scopo

Il Microsoft Interface Definition Language (MIDL) definisce le interfacce tra i programmi client e server. Microsoft include il compilatore MIDL con Platform Software Development Kit (SDK) per consentire agli sviluppatori di creare i file IDL (Interface Definition Language) e i file di configurazione dell'applicazione (ACF) necessari per le interfacce RPC (Remote Procedure Call) e le interfacce COM/DCOM. MIDL supporta anche la generazione di librerie dei tipi per l'automazione OLE.

## <a name="where-applicable"></a>Se applicabile

MIDL può essere usato in tutte le applicazioni client/server basate Windows sistemi operativi. Può essere usato anche per creare programmi client e server per ambienti di rete eterogenei che includono sistemi operativi come Unix e Apple. Microsoft supporta lo standard DCE Open Group (precedentemente noto come Open Software Foundation) DCE per l'interoperabilità RPC.

## <a name="developer-audience"></a>Sviluppatori

Quando si usa MIDL con RPC, è necessaria una certa familiarità con la programmazione C/C++ e il paradigma RPC. Quando si usa MIDL con COM, è necessaria una certa familiarità con la programmazione C++ e il paradigma RPC in quanto si applica a COM oppure, in alternativa, è necessaria una certa familiarità con le librerie dei tipi e gli script del modello di automazione OLE.

## <a name="run-time-requirements"></a>Requisiti di runtime

Le librerie di runtime appropriate per l'uso di MIDL sono incluse in Windows. Il compilatore MIDL e i componenti dell'ambiente di sviluppo RPC vengono installati quando si installa Windows SDK. Per altre informazioni, vedere [Uso del compilatore MIDL](using-the-midl-compiler-2.md) e [Installazione dell'ambiente di programmazione RPC.](/windows/desktop/Rpc/installing-the-rpc-programming-environment)

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                               | Descrizione                                                                        |
|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [Overview](about-this-guide-2.md)<br/>                                                       | Informazioni generali su MIDL e sul compilatore MIDL.<br/>                   |
| [Uso del compilatore MIDL](using-the-midl-compiler-2.md)<br/>                                 | Informazioni sull'uso della compilazione MIDL per generare stub RPC.<br/>       |
| [Definizioni di interfaccia e librerie dei tipi](interface-definitions-and-type-libraries.md)<br/> | Documentazione delle definizioni di interfaccia e delle librerie dei tipi specifiche di RPC.<br/> |
| [Informazioni di riferimento Command-Line MIDL](midl-command-line-reference.md)<br/>                           | Documentazione delle opzioni della riga di comando del compilatore MIDL.<br/>               |
| [Informazioni di riferimento sul linguaggio MIDL](midl-language-reference.md)<br/>                                   | Informazioni di riferimento sul linguaggio del compilatore MIDL.<br/>                                   |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Rpc (Remote Procedure Call)](/windows/desktop/Rpc/rpc-start-page)
</dt> </dl>

 

