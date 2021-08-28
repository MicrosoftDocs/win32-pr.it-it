---
title: Funzione type_UserSize
description: La funzione \_ UserSize di tipo è una funzione helper per gli attributi \ wire \_ marshal\ e \ user \_ marshal\.
ms.assetid: 74a46418-1a02-47ed-a3ab-35f3364cc38f
keywords:
- type_UserSize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2f997d12e11f643eb2faf9990454a8508d15636
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122886035"
---
# <a name="the-type_usersize-function"></a>Funzione \_ UserSize di tipo

La **&lt; funzione &gt; \_ UserSize di** tipo è una funzione helper per gli attributi wire \[ [ \_ marshal](/windows/desktop/Midl/wire-marshal) \] e user \[ [ \_ marshal.](/windows/desktop/Midl/user-marshal) \] Gli stub chiamano questa funzione per ridimensionare il buffer di dati RPC per l'oggetto dati utente prima che venga effettuato il marshalling dei dati sul lato client o server. La funzione è definita come:

``` syntax
unsigned long __RPC_USER  <type>_UserSize(
    unsigned long __RPC_FAR * pFlags,
    unsigned long StartingSize,
    <type>  __RPC_FAR *pMyObj);
```

Il &lt; tipo nel nome della funzione indica il tipo userm, come specificato nella definizione del tipo wire &gt; **\[ \_ marshal \]** o user **\[ \_ marshal. \]** Questo tipo può essere non ritrasmettibile o persino, se usato con l'attributo **\[ \_ di marshalling \]** utente, sconosciuto al compilatore MIDL. Il nome del tipo di cavo (il nome del tipo trasmesso in rete) non viene usato nel prototipo di funzione. Si noti, tuttavia, che il tipo wire definisce il layout per i dati come specificato da OSF DCE. Tutti i dati devono essere convertiti nel formato di rappresentazione dei dati di rete (NDR).

Il *parametro pFlags* è un puntatore a un campo flag **long** senza segno. La parola superiore del flag contiene flag di formato NDR come definito da DCE OSF per le rappresentazioni a virgola mobile, ordine dei byte e caratteri. La parola inferiore contiene un flag di contesto di marshalling come definito dal canale COM. Il layout esatto dei flag all'interno del campo è illustrato nella tabella seguente.



| BITS  | Flag                                  | valore                                                                                     |
|-------|---------------------------------------|-------------------------------------------------------------------------------------------|
| 31-24 | Rappresentazione a virgola mobile         | 0 = IEEE 1 = VAX 2 = Cray 3 = IBM                                                         |
| 23-20 | Ordine dei byte integer e a virgola mobile | 0 = Big-endian 1 = Little-endian                                                          |
| 19-16 | Rappresentazione dei caratteri              | 0 = ASCII 1 = EBCDIC                                                                      |
| 15-0  | Flag di contesto di marshalling               | 0 = MSHCTX \_ LOCAL 1 = MSHCTX \_ NOSHAREDMEM 2 = MSHCTX \_ DIFFERENTMACHINE 3 = MSHCTX \_ INPROC |



 

Il flag del contesto di marshalling consente di modificare il comportamento della routine a seconda del contesto per la chiamata RPC. Ad esempio, se si dispone di un handle (**long**) a un blocco di dati, è possibile inviare l'handle per una chiamata in-process, ma si inviano i dati effettivi per una chiamata a un computer diverso. Il flag del contesto di marshalling e i relativi valori sono definiti nei file Wtypes.h e Wtypes.idl in Platform Software Development Kit (SDK).

> [!Note]  
> Quando il tipo di collegamento è definito correttamente, non è necessario usare i flag di formato NDR, perché il motore NDR esegue le conversioni necessarie.

 

Il *parametro StartingSize* è l'offset del buffer corrente. La dimensione iniziale indica l'offset del buffer per l'oggetto utente e può essere allineata correttamente o meno. La routine deve prendere in considerazione la spaziatura interna necessaria.

Il *parametro pMyObj* è un puntatore a un oggetto di tipo utente.

Il valore restituito è il nuovo offset o posizione del buffer. La funzione deve restituire la dimensione cumulativa, ovvero la dimensione iniziale più la possibile spaziatura interna più le dimensioni dei dati.

La **&lt; funzione &gt; \_ UserSize** di tipo può restituire una sovrastima delle dimensioni necessarie. Le dimensioni effettive del buffer inviato sono definite dalle dimensioni dei dati, non dalla dimensione di allocazione del buffer.

La **&lt; funzione &gt; \_ UserSize di** tipo non viene chiamata se le dimensioni del cavo possono essere calcolate in fase di compilazione. Si noti che per la maggior parte delle unioni, anche se non sono presenti puntatori, le dimensioni effettive della rappresentazione cablata possono essere determinate solo in fase di esecuzione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Regole di marshalling per il \_ marshalling utente e il \_ marshalling del wire](marshaling-rules-for-user-marshal-and-wire-marshal.md)
</dt> <dt>

[marshalling \_ utente](/windows/desktop/Midl/user-marshal)
</dt> <dt>

[wire \_ marshal](/windows/desktop/Midl/wire-marshal)
</dt> </dl>

 

 
