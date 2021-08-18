---
title: range (attributo)
description: L'attributo \ range\ consente di specificare un intervallo di valori consentiti per argomenti o campi i cui valori vengono impostati in fase di esecuzione. Se usato con un tipo di pipe, l'attributo specifica l'intervallo consentito per il conteggio degli elementi nei blocchi di pipe.
ms.assetid: 1609fea5-e82c-4389-b4f4-2cd8d0622cde
keywords:
- Attributo range MIDL
topic_type:
- apiref
api_name:
- range
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8be59ef1b212d0f6953063ce7ac3239d8940a5ea54a623990fc3d7af9f36ad3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764311"
---
# <a name="range-attribute"></a>range (attributo)

**\[ L'attributo \]** range consente di specificare un intervallo di valori consentiti per argomenti o campi i cui valori sono impostati in fase di esecuzione. Se usato con un tipo di pipe, l'attributo specifica l'intervallo consentito per il conteggio degli elementi nei blocchi di pipe.

``` syntax
[range(low-val,high-val)] type-specifier declarator
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*low-val* 
</dt> <dd>

Valore minimo consentito che il parametro o il campo può contenere.

</dd> <dt>

*high-val* 
</dt> <dd>

Valore massimo consentito che il parametro o il campo può contenere.

</dd> <dt>

*type-specifier* 
</dt> <dd>

Un tipo integrale diverso da [**hyper**](hyper.md) o [**\_ \_ int64**](--int64.md), un identificatore di tipo per un tipo integrale, un [**tipo enum**](enum.md) o un nome di tipo pipe.

</dd> <dt>

*Dichiaratore* 
</dt> <dd>

Dichiaratore C standard, ad esempio un identificatore.

</dd> </dl>

## <a name="remarks"></a>Commenti

Usare l'attributo **\[ range \]** per modificare il significato di parametri o campi sensibili, ad esempio quelli usati per le dimensioni o la lunghezza, con matrici conformi o variabili oppure ogni volta che si vuole controllare un parametro o un valore di campo rispetto a un intervallo di valori validi. L'attributo è applicabile ai parametri di primo livello, nonché ai parametri e ai campi di livello inferiore. **\[ L'aggiunta \] dell'attributo** range a un tipo non ne modifica il formato di collegamento, pertanto non influisce sulla compatibilità con le versioni precedenti.

**\[ L'attributo \]** range può essere usato anche su dati conformi, ad esempio buffer o matrici con un attributo di conformità. L'effetto è limitare tutte le dimensioni di conformità per i dati conformi all'intervallo specificato. Se i dati conformi sono una matrice multidimensionale, ogni dimensione della matrice è limitata all'intervallo specificato.

**\[ L'uso \] dell'intervallo** sui dati conformi richiede che la destinazione di compilazione sia â€"target NT60 o versione successiva.

Si noti che è necessario usare l'opzione del compilatore [**/robust**](-robust.md) quando si compila il file IDL per generare il codice stub che eseguirà questi controlli. Senza **l'opzione /robust,** il compilatore MIDL ignora questo attributo.

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

[**il \_ primo è**](first-is.md)
</dt> <dt>

[**\_l'ultimo è**](last-is.md)
</dt> <dt>

[**length \_ è**](length-is.md)
</dt> <dt>

[**max \_ è**](max-is.md)
</dt> <dt>

[**/robust**](-robust.md)
</dt> <dt>

[**size \_ è**](size-is.md)
</dt> <dt>

[**\_l'opzione è**](switch-is.md)
</dt> </dl>

 

 