---
title: Funzione type_UserSize
description: Il tipo \_ UserSize Function è una funzione di supporto per gli attributi \ Wire \_ Marshal \ e \ User \_ Marshal \.
ms.assetid: 74a46418-1a02-47ed-a3ab-35f3364cc38f
keywords:
- type_UserSize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a29e5936763f9fe7b3513d66ddca7db9c35dbfe7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103730018"
---
# <a name="the-type_usersize-function"></a>Funzione di tipo \_ UserSize

La funzione **<type> \_ UserSize** è una funzione di supporto per il \[ [ \_ marshalling di rete](/windows/desktop/Midl/wire-marshal) \] e \[ gli attributi del [ \_ marshalling degli utenti](/windows/desktop/Midl/user-marshal) \] . Gli stub chiamano questa funzione per ridimensionare il buffer di dati RPC per l'oggetto dati utente prima che venga eseguito il marshalling dei dati sul lato client o server. La funzione è definita come segue:

``` syntax
unsigned long __RPC_USER  <type>_UserSize(
    unsigned long __RPC_FAR * pFlags,
    unsigned long StartingSize,
    <type>  __RPC_FAR *pMyObj);
```

<type>Nel nome della funzione corrisponde a User-Type, come specificato nella definizione del **\[ \_ marshalling \] di rete** o del tipo di **\[ \_ \] marshalling dell'utente** . Questo tipo può essere untransmittable o even, se usato con l'attributo **\[ \_ Marshal \] dell'utente** , sconosciuto al compilatore MIDL. Il nome del tipo Wire (il nome del tipo trasmesso attraverso la rete) non viene utilizzato nel prototipo di funzione. Si noti, tuttavia, che il tipo Wire definisce il layout per i dati come specificato da OSF DCE. Tutti i dati devono essere convertiti nel formato di rappresentazione dei dati di rete (NDR).

Il parametro *pFlags* è un puntatore a un campo **unsigned long** flag. La parola superiore del flag contiene i flag di formato NDR come definito da OSF DCE per la virgola mobile, l'ordine dei byte e le rappresentazioni di caratteri. La parola inferiore contiene un flag di contesto di marshalling definito dal canale COM. La tabella seguente illustra il layout esatto dei flag all'interno del campo.



| BITS  | Flag                                  | valore                                                                                     |
|-------|---------------------------------------|-------------------------------------------------------------------------------------------|
| 31-24 | Rappresentazione a virgola mobile         | 0 = IEEE 1 = VAX 2 = Cray 3 = IBM                                                         |
| 23-20 | Ordine di byte Integer e a virgola mobile | 0 = big-endian 1 = little-endian                                                          |
| 19-16 | Rappresentazione di caratteri              | 0 = ASCII 1 = EBCDIC                                                                      |
| 15-0  | Flag di contesto di marshalling               | 0 = MSHCTX \_ Local 1 = MSHCTX \_ NOSHAREDMEM 2 = MSHCTX \_ DIFFERENTMACHINE 3 = MSHCTX \_ InProc |



 

Il flag di contesto del marshalling rende possibile la modifica del comportamento della routine a seconda del contesto della chiamata RPC. Se, ad esempio, si dispone di un handle (**Long**) per un blocco di dati, è possibile inviare l'handle per una chiamata in-process, ma inviare i dati effettivi per una chiamata a un altro computer. Il flag del contesto di marshalling e i relativi valori sono definiti nei file wtypes. h e wtypes. idl di Platform Software Development Kit (SDK).

> [!Note]  
> Quando il tipo di trasmissione è definito correttamente, non è necessario usare i flag di formato NDR, perché il motore di NDR esegue le conversioni necessarie.

 

*StartingSize* un parametro è l'offset del buffer corrente. La dimensione iniziale indica l'offset del buffer per l'oggetto utente e può essere allineato o meno correttamente. La routine dovrebbe tenere conto del riempimento necessario.

Il parametro *pMyObj* è un puntatore a un oggetto tipo utente.

Il valore restituito è il nuovo offset o la nuova posizione del buffer. La funzione deve restituire la dimensione cumulativa, ovvero le dimensioni iniziali più la spaziatura interna più la dimensione dei dati.

La funzione **<type> \_ UserSize** può restituire una sovrastima delle dimensioni necessarie. La dimensione effettiva del buffer inviato è definita dalle dimensioni dei dati, non dalle dimensioni di allocazione del buffer.

La funzione **<type> \_ UserSize** non viene chiamata se le dimensioni del Wire possono essere calcolate in fase di compilazione. Si noti che per la maggior parte delle unioni, anche se non sono presenti puntatori, le dimensioni effettive della rappresentazione in transito possono essere determinate solo in fase di esecuzione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Regole di marshalling per \_ marshalling utente e \_ marshalling di rete](marshaling-rules-for-user-marshal-and-wire-marshal.md)
</dt> <dt>

[\_marshalling utente](/windows/desktop/Midl/user-marshal)
</dt> <dt>

[\_marshalling di rete](/windows/desktop/Midl/wire-marshal)
</dt> </dl>

 

 