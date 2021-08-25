---
title: Opzione /robust
description: L'opzione /robust indica al compilatore MIDL di generare informazioni aggiuntive sul controllo degli errori, che il motore NDR usa per eseguire controlli di integrità in fase di esecuzione.
ms.assetid: 7a858600-ea06-4396-9a1b-240d646e8c7d
keywords:
- Opzione /robust MIDL
topic_type:
- apiref
api_name:
- /robust
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 551f5a60013aa3a903dcb3e35cc4c25a9f83dc67fff2a6ab5c7bfd62a041feee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119895821"
---
# <a name="robust-switch"></a>Opzione /robust

**L'opzione /robust** indica al compilatore MIDL di generare informazioni aggiuntive sul controllo degli errori, che il motore NDR usa per eseguire controlli di integrità in fase di esecuzione.

``` syntax
midl /robust {/Oicf | /Oif }
```

## <a name="switch-options"></a>Opzioni di cambio

<dl> <dt>

*/Oicf* 
</dt> <dd></dd> <dt>

*/Oif* 
</dt> <dd>

Queste opzioni sono identiche nelle relative funzionalità. Specificano il metodo proxy senza codice di marshalling e usano stringhe di formato rapido per migliorare le prestazioni. Vedere / [**Oi**](-oi.md).

</dd> </dl>

## <a name="remarks"></a>Commenti

L'uso dell'opzione **/robust** genera informazioni aggiuntive che consentono al motore di rappresentazione dei dati di rete (NDR) di eseguire il controllo degli errori di runtime sugli argomenti correlati in matrici dinamiche, unioni e puntatori a interfaccia [**in**](out-idl.md) uscita nelle applicazioni DCOM. **L'opzione /robust** è disponibile solo in Windows 2000 e versioni successive di Windows.

Un argomento correlato è un argomento che usa uno degli attributi che consentono di determinare le dimensioni di un oggetto dati in fase di esecuzione: [**size \_ è**](size-is.md), [**length \_ è**](length-is.md), [**first \_ è**](first-is.md), [**last \_ è**](last-is.md), [**max \_ è**](max-is.md), switch è e [**iid \_ è**](iid-is.md). [**\_**](switch-is.md) In conformità con la specifica OSF-DCE per la rappresentazione cablata, questo argomento correlato viene visualizzato in due posizioni diverse. Si consideri, ad esempio, un utilizzo tipico delle **dimensioni \_ è l'attributo** :

``` syntax
HRESULT Func1([in] long Size, 
              [in, size_is(Size)]BAR_TYPE *pBarType);
```

In questo esempio, il client passa un valore long che specifica le dimensioni di un blocco di TIPI DI BARRA (in termini di numero di elementi BAR TYPES) e un puntatore al blocco effettivo di TIPI DI \_ \_ \_ BARRA. L'argomento Size è correlato all'argomento pBarType. In base alla specifica OSF-DCE, l'argomento Size viene rappresentato due volte in transito, prima come se stesso e quindi con la matrice di elementi BAR TYPE che rappresentano l'argomento \_ pBarType. Ogni argomento viene disassociato in modo indipendente, in base alla relativa rappresentazione di collegamento. In genere, l'argomento Size e la relativa copia, che viene usata per rappresentare parte dell'altro argomento, hanno gli stessi valori. Tuttavia, se l'argomento Size viene danneggiato(ad esempio, quando il blocco di BAR TYPES è maggiore di quello allocato), l'applicazione server potrebbe smettere di rispondere, perché usa il valore dell'argomento Size per misurare i dati in \_ ingresso.

**L'opzione /robust** è necessaria per implementare il controllo dell'intervallo valido con l'attributo [**range.**](range.md)

## <a name="examples"></a>Esempio

**midl /robust /Oicf filename.idl**

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Sintassi della riga di comando MIDL generale](general-midl-command-line-syntax.md)
</dt> <dt>

[**/oi**](-oi.md)
</dt> <dt>

[**Gamma**](range.md)
</dt> </dl>

 

 




