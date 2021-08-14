---
title: Intestazione
description: L'intestazione seguente rappresenta uno degli stili di intestazione che possono essere generati dalla versione corrente di MIDL. Per praticità, l'elenco completo dei campi di intestazione è disponibile qui.
ms.assetid: 2078d2d9-1757-4449-9cc1-a21804654722
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b27ee00425f3611234b0cd001f254b1499a0d4873d05846c65a2828c3eeffe57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118924540"
---
# <a name="the-header"></a>Intestazione

L'intestazione seguente rappresenta uno degli stili di intestazione che possono essere generati dalla versione corrente di MIDL. Per praticità, l'elenco completo dei campi di intestazione è disponibile qui.

([**intestazione –Oif)**](/windows/desktop/Midl/-oi)

``` syntax
handle_type<1> 
Oi_flags<1>
[rpc_flags<4>]
proc_num<2>  
stack_size<2>
[explicit_handle_description<>]
constant_client_buffer_size<2>
constant_server_buffer_size<2>
INTERPRETER_OPT_FLAGS<1>
number_of_params<1>
```

Estensioni a partire da Windows 2000: <8> per 32 bit, <12> per 64 bit)

``` syntax
extension_version<1>
INTERPRETER_OPT_FLAGS2<1>
ClientCorrHint<2>
ServerCorrHint<2>
NotifyIndex<2>
[ FloatDoubleMask<2> ]
```

La versione \_ dell'<1> specifica le dimensioni della sezione dell'estensione, in byte. In questo modo il motore NDR corrente può eseguire correttamente il passaggio della sezione dell'estensione anche se la sezione deriva da una versione successiva del compilatore con più campi di quelli che il motore corrente è in grado di comprendere.

I FLAG INTERPRETER \_ \_ OPT2 sono definiti come segue:

``` syntax
typedef struct
  {
  unsigned char   HasNewCorrDesc      : 1;    // 0x01
  unsigned char   ClientCorrCheck     : 1;    // 0x02
  unsigned char   ServerCorrCheck     : 1;    // 0x04
  unsigned char   HasNotify           : 1;    // 0x08
  unsigned char   HasNotify2          : 1;    // 0x10
  unsigned char   Unused              : 3;
  } INTERPRETER_OPT_FLAGS2, *PINTERPRETER_OPT_FLAGS2;
```

Il **membro HasNewCorrDesc** indica se vengono usati nuovi descrittori di correlazione nelle stringhe di formato generate dal compilatore. Il nuovo descrittore di correlazione è correlato alla funzionalità denial of attack. I **membri ClientCorrCheck** e **ServerCorrCheck** vengono impostati quando la routine richiede il controllo di correlazione sul lato indicato.

I **flag HasNotify** e **HasNotify2** indicano che la routine usa la funzionalità di notifica come definito rispettivamente dagli attributi **\[ del \]** **\[ \_ flag \]** notify e notify.

Il **membro ClientCorrCheck** è un hint per le dimensioni della cache sul lato client e **ServerCorrCheck** è un hint sul lato server. Quando le dimensioni sono pari a zero, è consigliabile usare una dimensione predefinita.

**L'elemento NotifyIndex** è un indice di una routine notify, se ne viene usata una.

**L'elemento FloatDoubleMask** risolve il problema di un argomento a virgola mobile per le Windows a 64 bit. Questo campo viene generato solo per gli stub a 64 bit. La maschera è necessaria per le routine di assembly che scaricano/caricano registri da/verso lo stack virtuale per gestire correttamente gli argomenti a virgola mobile e i registri. La maschera è costituita da 2 bit per argomento o piuttosto da ogni registro a virgola mobile. Il codice è il seguente: i bit meno significativi corrispondono al primo registro FP, i 2 bit successivi corrispondono al secondo registro e così via.

> [!Note]  
> Per le routine oggetto, il primo argomento finisce nel secondo registro perché questo puntatore è il primo. Per ogni registro il significato dei bit è come illustrato nella tabella seguente.

 



| BITS | Significato                                          |
|------|--------------------------------------------------|
| 01   | Un valore float deve essere caricato nel registro.  |
| 10   | Un valore double deve essere caricato nel registro. |



 

00 e 11 sono valori non validi per i bit.

Attualmente sono presenti otto registri FP in un processore Intel Architecture a 64 bit, quindi la maschera può avere solo 16b bit più bassi impostati. La dimensione della maschera è stata impostata su un totale di 16 bit in base alla maschera del compilatore C che rimane invariata.

## <a name="header-streamlining-for-performance"></a>Ottimizzazione delle intestazioni per le prestazioni

Per semplificare il codice e migliorare le prestazioni, il compilatore tenta di generare un'intestazione a dimensione fissa quando possibile. In particolare, per DCOM asincrono viene usata l'intestazione seguente:

``` syntax
typedef struct _NDR_DCOM_OI2_PROC_HEADER
  {
  unsigned char               HandleType;        // The Oi header
  INTERPRETER_FLAGS           OldOiFlags;        //
  unsigned short              RpcFlagsLow;       //
  unsigned short              RpcFlagsHi;        //
  unsigned short              ProcNum;           //
  unsigned short              StackSize;         //
  // expl handle descr is never generated        //
  unsigned short              ClientBufferSize;  // The Oi2 header
  unsigned short              ServerBufferSize;  //
  INTERPRETER_OPT_FLAGS       Oi2Flags;          //
  unsigned char               NumberParams;      //
  } NDR_DCOM_OI2_PROC_HEADER, *PNDR_DCOM_OI2_PROC_HEADER;
```

 

 