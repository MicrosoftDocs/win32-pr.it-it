---
title: Tipi di base
description: Per evitare i problemi che i tipi di dati dipendenti dall'implementazione possono causare in architetture di computer diverse, MIDL definisce i propri tipi di dati di base.
ms.assetid: 0b2778c7-8cee-415f-bb5e-01f6c9eedc70
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1aadc1ae5fedd73a01ce0fd7ed735689e043cff0d74910175cf2ab691c22eeed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120023281"
---
# <a name="base-types"></a>Tipi di base

Per evitare i problemi che i tipi di dati dipendenti dall'implementazione possono causare in architetture di computer diverse, MIDL definisce i propri tipi di dati di base.



| Tipo base                         | Descrizione                                                                                                                                                         |
|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**boolean**](/windows/desktop/Midl/boolean)       | Elemento di dati che può avere il valore **TRUE** o **FALSE.**                                                                                                          |
| [**byte**](/windows/desktop/Midl/byte)             | Un elemento di dati a 8 bit è garantito per la trasmissione senza modifiche.                                                                                                 |
| [**Char**](/windows/desktop/Midl/char-idl)         | Elemento di dati carattere senza segno a 8 bit.                                                                                                                              |
| [**Doppia**](/windows/desktop/Midl/double)         | Numero a virgola mobile a 64 bit.                                                                                                                                     |
| [**Galleggiante**](/windows/desktop/Midl/float)           | Numero a virgola mobile a 32 bit.                                                                                                                                     |
| [**handle \_ t**](/windows/desktop/Midl/handle-t)    | Handle primitivo che può essere utilizzato per l'associazione RPC o la serializzazione dei dati.                                                                                            |
| [**hyper**](/windows/desktop/Midl/hyper)           | Un intero a 64 bit che può essere dichiarato come [**signed**](/windows/desktop/Midl/signed) o [**unsigned**](/windows/desktop/Midl/unsigned) Può anche essere definito **\_ int64**.                  |
| [**int**](/windows/desktop/Midl/int)               | Intero a 32 bit che può essere dichiarato come **con o** **senza segno.**                                                                                         |
| [**\_\_int3264**](/windows/desktop/Midl/--int3264) | Parola chiave che specifica un tipo integrale con proprietà a 32 bit o a 64 bit.                                                                              |
| [**long**](/windows/desktop/Midl/long)             | Modificatore per **int** che indica un intero a 32 bit. Può essere dichiarato come **con o** **senza segno.**                                                       |
| [**short**](/windows/desktop/Midl/short)           | Intero a 16 bit che può essere dichiarato come **con o** **senza segno.**                                                                                         |
| [**Piccolo**](/windows/desktop/Midl/small)           | Modificatore per **int** che indica un intero a 8 bit. Può essere dichiarato come **con o** **senza segno.**                                                       |
| [**wchar \_ t**](/windows/desktop/Midl/wchar-t)      | Tipo di carattere wide supportato come estensione Microsoft per IDL. Pertanto, questo tipo non è disponibile se si esegue la compilazione usando [ / **l'opzione osf.**](/windows/desktop/Midl/-osf) |



 

Il file di intestazione Rpcndr.h fornisce le definizioni per la maggior parte di questi tipi di dati di base. La parola **chiave int** è riconosciuta ed è trasmissibile su piattaforme a 32 bit. Nelle piattaforme a 16 bit il tipo di dati **int** richiede un modificatore, ad esempio **short** o **long**, per specificarne la lunghezza.

Sebbene **\* \* void** sia riconosciuto come tipo puntatore generico dallo standard ANSI C, MIDL ne limita l'utilizzo. Ogni puntatore usato in un'operazione remota o di serializzazione deve puntare a tipi di base o tipi costruiti da tipi di base. Esiste un'eccezione: gli handle di contesto sono definiti come **tipi void.** Per altre informazioni, vedere [Handle di contesto.](context-handles.md)

 

 