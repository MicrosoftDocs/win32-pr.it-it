---
title: Tipi di base
description: Per evitare i problemi che i tipi di dati dipendenti dall'implementazione possono causare su diverse architetture di computer, MIDL definisce i propri tipi di dati di base.
ms.assetid: 0b2778c7-8cee-415f-bb5e-01f6c9eedc70
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50ee57261aac1de6ea4bb15c9a4550721dd10282
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338951"
---
# <a name="base-types"></a>Tipi di base

Per evitare i problemi che i tipi di dati dipendenti dall'implementazione possono causare su diverse architetture di computer, MIDL definisce i propri tipi di dati di base.



| Tipo base                         | Descrizione                                                                                                                                                         |
|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**boolean**](/windows/desktop/Midl/boolean)       | Elemento di dati il cui valore può essere **true** o **false**.                                                                                                          |
| [**byte**](/windows/desktop/Midl/byte)             | Un elemento di dati a 8 bit garantisce la trasmissione senza alcuna modifica.                                                                                                 |
| [**char**](/windows/desktop/Midl/char-idl)         | Elemento dati di tipo carattere senza segno a 8 bit.                                                                                                                              |
| [**doppio**](/windows/desktop/Midl/double)         | Numero a virgola mobile a 64 bit.                                                                                                                                     |
| [**float**](/windows/desktop/Midl/float)           | Numero a virgola mobile a 32 bit.                                                                                                                                     |
| [**handle \_ t**](/windows/desktop/Midl/handle-t)    | Handle primitivo che può essere utilizzato per l'associazione RPC o la serializzazione dei dati.                                                                                            |
| [**Hyper**](/windows/desktop/Midl/hyper)           | Un intero a 64 bit che può essere dichiarato come con [**segno**](/windows/desktop/Midl/signed) o [**senza segno**](/windows/desktop/Midl/unsigned) può anche essere definito **\_ Int64**.                  |
| [**INT**](/windows/desktop/Midl/int)               | Intero A 32 bit che può essere dichiarato come con segno **o** **senza segno**.                                                                                         |
| [**\_\_int3264**](/windows/desktop/Midl/--int3264) | Parola chiave che specifica un tipo integrale con proprietà a 32 bit o a 64 bit.                                                                              |
| [**long**](/windows/desktop/Midl/long)             | Modificatore per **int** che indica un intero a 32 bit. Può essere dichiarato come con **segno** o **senza segno**.                                                       |
| [**short**](/windows/desktop/Midl/short)           | Intero A 16 bit che può essere dichiarato come con segno **o** **senza segno**.                                                                                         |
| [**piccolo**](/windows/desktop/Midl/small)           | Modificatore per **int** che indica un intero a 8 bit. Può essere dichiarato come con **segno** o **senza segno**.                                                       |
| [**WCHAR \_ t**](/windows/desktop/Midl/wchar-t)      | Tipo a caratteri wide supportato come estensione Microsoft per IDL. Pertanto, questo tipo non è disponibile se si compila utilizzando l'opzione [ / **OSF**](/windows/desktop/Midl/-osf) . |



 

Il file di intestazione Rpcndr. h fornisce le definizioni per la maggior parte di questi tipi di dati di base. La parola chiave **int** è riconosciuta e può essere trasmessa in piattaforme a 32 bit. Nelle piattaforme a 16 bit il tipo di dati **int** richiede un modificatore, ad esempio **short** o **Long**, per specificarne la lunghezza.

Sebbene **void \* \*** venga riconosciuto come tipo di puntatore generico dallo standard ANSI C, MIDL ne limita l'utilizzo. Ogni puntatore utilizzato in un'operazione remota o di serializzazione deve puntare ai tipi di base o ai tipi costruiti dai tipi di base. (Si verifica un'eccezione: gli handle di contesto sono definiti come tipi **void** . Per ulteriori informazioni, vedere [handle di contesto](context-handles.md).

 

 