---
title: Intestazione
description: L'intestazione seguente rappresenta uno degli stili di intestazione che possono essere generati dalla versione corrente di MIDL. Per praticità, l'elenco completo dei campi di intestazione è disponibile qui.
ms.assetid: 2078d2d9-1757-4449-9cc1-a21804654722
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0afcc9ad880278fdbcb8efc45fdabdc22ad06224
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103872886"
---
# <a name="the-header"></a>Intestazione

L'intestazione seguente rappresenta uno degli stili di intestazione che possono essere generati dalla versione corrente di MIDL. Per praticità, l'elenco completo dei campi di intestazione è disponibile qui.

(Intestazione [**-OIF**](/windows/desktop/Midl/-oi) )

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

Estensioni a partire da Windows 2000: <8> per 32 bit <12> per 64 bit)

``` syntax
extension_version<1>
INTERPRETER_OPT_FLAGS2<1>
ClientCorrHint<2>
ServerCorrHint<2>
NotifyIndex<2>
[ FloatDoubleMask<2> ]
```

La versione dell'estensione \_<1> fornisce la dimensione, in byte, della sezione di estensione. In questo modo, il motore di NDR corrente può eseguire correttamente l'istruzione/routine della sezione dell'estensione anche se la sezione deve provenire da una versione del compilatore successiva con più campi rispetto al motore corrente.

L'INTERPRETe \_ opt \_ FLAGS2 è definito come segue:

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

Il membro **HasNewCorrDesc** indica se vengono utilizzati nuovi descrittori di correlazione nelle stringhe di formato generate dal compilatore. Il nuovo descrittore di correlazione è correlato alla funzionalità di negazione dell'attacco. I membri **ClientCorrCheck** e **ServerCorrCheck** vengono impostati quando la routine richiede il controllo della correlazione sul lato indicato.

I flag **HasNotify** e **HasNotify2** indicano che la routine usa la funzionalità Notify come definito dagli attributi **\[ Notify \]** e **\[ Notify \_ flag \]** , rispettivamente.

Il membro **ClientCorrCheck** è un hint per la dimensione della cache sul lato client e **ServerCorrCheck** è un suggerimento sul lato server. Quando la dimensione è pari a zero, è necessario usare una dimensione predefinita.

L'elemento **NotifyIndex** è un indice di una routine Notify, se ne viene utilizzato uno.

L'elemento **FloatDoubleMask** risolve il problema di un argomento a virgola mobile per Windows a 64 bit. Questo campo viene generato solo per gli stub a 64 bit. La maschera è necessaria per le routine di assembly che scaricano/caricano i registri da/nello stack virtuale per gestire gli argomenti a virgola mobile e vengono registrati correttamente. La maschera è costituita da 2 bit per argomento o piuttosto per ogni registro a virgola mobile. Il codice è il seguente: i bit meno significativi corrispondono al primo registro FP, i 2 bit successivi corrispondono al secondo registro e così via.

> [!Note]  
> Per le routine degli oggetti, il primo argomento finisce nel secondo registro a causa del primo puntatore. Per ogni registro il significato di BITS è come illustrato nella tabella seguente.

 



| BITS | Significato                                          |
|------|--------------------------------------------------|
| 01   | È necessario caricare un valore float nel registro.  |
| 10   | È necessario caricare un valore Double nel registro. |



 

00 e 11 sono valori non validi per i bit.

Attualmente sono presenti otto registri FP in un processore Intel Architecture a 64 bit, di conseguenza la maschera può avere solo 16B bit più bassi impostati. Le dimensioni della maschera sono state impostate su un totale di 16 bit in base alla maschera del compilatore C rimanente invariato.

## <a name="header-streamlining-for-performance"></a>Ottimizzazione delle intestazioni per le prestazioni

Per semplificare il codice e migliorare le prestazioni, il compilatore tenta di generare un'intestazione a dimensione fissa quando possibile. In particolare, viene utilizzata l'intestazione seguente per DCOM asincrono:

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

 

 