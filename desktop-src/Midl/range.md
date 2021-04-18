---
title: range (attributo)
description: L'attributo \ range \ consente di specificare un intervallo di valori consentiti per argomenti o campi i cui valori sono impostati in fase di esecuzione. Quando viene usato con un tipo di pipe, l'attributo specifica l'intervallo consentito per il numero di elementi nei blocchi di pipe.
ms.assetid: 1609fea5-e82c-4389-b4f4-2cd8d0622cde
keywords:
- attributo di intervallo MIDL
topic_type:
- apiref
api_name:
- range
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e095d420afc433c1f01a63dff51868e57efc50f4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299633"
---
# <a name="range-attribute"></a>range (attributo)

L'attributo **\[ Range \]** consente di specificare un intervallo di valori consentiti per gli argomenti o i campi i cui valori vengono impostati in fase di esecuzione. Quando viene usato con un tipo di pipe, l'attributo specifica l'intervallo consentito per il numero di elementi nei blocchi di pipe.

``` syntax
[range(low-val,high-val)] type-specifier declarator
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*bassa Val* 
</dt> <dd>

Valore minimo consentito che il parametro o il campo può tenere.

</dd> <dt>

*alta Val* 
</dt> <dd>

Valore massimo consentito che il parametro o il campo può tenere.

</dd> <dt>

*identificatore di tipo* 
</dt> <dd>

Un tipo integrale diverso da [**Hyper**](hyper.md) o [**\_ \_ Int64**](--int64.md), un identificatore di tipo a un tipo integrale, un tipo [**enum**](enum.md) o un nome di tipo di pipe.

</dd> <dt>

*dichiaratore* 
</dt> <dd>

Dichiaratore C standard, ad esempio un identificatore.

</dd> </dl>

## <a name="remarks"></a>Commenti

Usare l'attributo **\[ Range \]** per modificare il significato dei parametri sensibili o dei campi, ad esempio quelli usati per le dimensioni o la lunghezza, con matrici conformi o variabili; oppure ogni volta che si vuole controllare un parametro o un valore di campo rispetto a un intervallo di valori validi. L'attributo è applicabile ai parametri di primo livello, oltre ai parametri e ai campi di livello inferiore. L'aggiunta dell'attributo di **\[ intervallo \]** a un tipo non comporta la modifica del formato wire, quindi non influisce sulla compatibilità con le versioni precedenti.

L'attributo **\[ Range \]** può essere usato anche su dati conformi, ad esempio buffer o matrici con un attributo di conformità. L'effetto è quello di limitare tutte le dimensioni di conformità per i dati conformi all'intervallo specificato. Se i dati conformi sono matrici multidimensionali, ogni dimensione della matrice è limitata all'intervallo specificato.

Per usare l' **\[ intervallo \]** nei dati conformi, è necessario che la destinazione della compilazione sia "$" di destinazione nt60 o versione successiva.

Si noti che è necessario usare l'opzione del compilatore [**/robust**](-robust.md) quando si compila il file IDL per generare il codice stub che eseguirà questi controlli. Senza l'opzione **/robust** , il compilatore MIDL ignora questo attributo.

## <a name="examples"></a>Esempi

``` syntax
HRESULT Method1(
    [in, range(0,100)] ULONG m,
    [in, range(0,100)] ULONG n,
    [size_is(m,n)] ULONG **pplong);

void InPipe(
    [in, range(0, MAX_CHUNK) LONG_PIPE pipe_date);
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[File di definizione dell'interfaccia (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[matrici](/windows/desktop/Rpc/arrays)
</dt> <dt>

[**il primo \_ è**](first-is.md)
</dt> <dt>

[**ultimo \_ è**](last-is.md)
</dt> <dt>

[**lunghezza \_**](length-is.md)
</dt> <dt>

[**Max \_ è**](max-is.md)
</dt> <dt>

[**/Robust**](-robust.md)
</dt> <dt>

[**dimensioni \_**](size-is.md)
</dt> <dt>

[**opzione \_**](switch-is.md)
</dt> </dl>

 

 