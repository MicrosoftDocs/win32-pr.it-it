---
title: opzione/robust
description: L'opzione/robust indica al compilatore MIDL di generare ulteriori informazioni sul controllo degli errori, utilizzate dal motore di recapito dell'integrità per eseguire controlli di integrità in fase di esecuzione.
ms.assetid: 7a858600-ea06-4396-9a1b-240d646e8c7d
keywords:
- /Robust switch MIDL
topic_type:
- apiref
api_name:
- /robust
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 974f9530006c03a041d9d444c41f9c5ca01569c0
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "103857238"
---
# <a name="robust-switch"></a>opzione/robust

L'opzione **/robust** indica al compilatore MIDL di generare ulteriori informazioni sul controllo degli errori, utilizzate dal motore di recapito dell'integrità per eseguire controlli di integrità in fase di esecuzione.

``` syntax
midl /robust {/Oicf | /Oif }
```

## <a name="switch-options"></a>Opzioni switch

<dl> <dt>

*/Oicf* 
</dt> <dd></dd> <dt>

*/OIF* 
</dt> <dd>

Queste opzioni sono identiche nelle rispettive funzionalità. Specificano il metodo proxy codificato per il marshalling e utilizzano stringhe di formato rapido per migliorare le prestazioni. Vedere/ [**OI**](-oi.md).

</dd> </dl>

## <a name="remarks"></a>Commenti

L'utilizzo dell'opzione **/robust** genera informazioni aggiuntive che consentono al motore di rappresentazione dei dati di rete (NDR) di eseguire il controllo degli errori di run-time sugli argomenti correlati in matrici dinamiche, unioni e puntatori di interfaccia in [**uscita**](out-idl.md) nelle applicazioni DCOM. L'opzione **/robust** è disponibile solo in Windows 2000 e versioni successive di Windows.

Un argomento correlato è un argomento che usa uno degli attributi che consentono di determinare la dimensione di un oggetto dati in fase di esecuzione: [**size \_ è**](size-is.md), [**length \_ è**](length-is.md), [**First \_ è**](first-is.md), [**Last \_ is**](last-is.md), [**Max \_ is**](max-is.md), [**Switch \_ is**](switch-is.md)e [**IID \_ è**](iid-is.md). In conformità con la specifica OSF-DCE per la rappresentazione Wire, questo argomento correlato viene visualizzato in due posizioni diverse. Si consideri, ad esempio, un utilizzo tipico della **dimensione \_ è** attribute:

``` syntax
HRESULT Func1([in] long Size, 
              [in, size_is(Size)]BAR_TYPE *pBarType);
```

In questo esempio, il client passa un valore Long che specifica la dimensione di un blocco di \_ tipi di barre (in termini di numero di elementi dei tipi di barre \_ ) e un puntatore al blocco effettivo dei tipi di barre \_ . L'argomento size è correlato all'argomento pBarType. In conformità con la specifica OSF-DCE, l'argomento di dimensione viene rappresentato due volte in rete, prima come se stesso e quindi con la matrice di \_ elementi di tipo barra che rappresentano l'argomento pBarType. Ogni argomento viene sottoposto a unmarshalling indipendentemente, in base alla propria rappresentazione in transito. In genere, l'argomento size e la relativa copia, usato per rappresentare parte dell'altro argomento, hanno gli stessi valori. Tuttavia, se l'argomento di dimensione viene danneggiato, ad esempio quando il blocco di tipi di barre \_ è maggiore di quello allocato, l'applicazione server potrebbe non rispondere, perché usa il valore dell'argomento size per misurare i dati in ingresso.

L'opzione **/robust** è necessaria per implementare il controllo dell'intervallo valido con l'attributo [**Range**](range.md) .

## <a name="examples"></a>Esempio

**MIDL/robust/Oicf nomefile. idl**

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Sintassi della riga di comando MIDL generale](general-midl-command-line-syntax.md)
</dt> <dt>

[**/OI**](-oi.md)
</dt> <dt>

[**intervallo**](range.md)
</dt> </dl>

 

 




