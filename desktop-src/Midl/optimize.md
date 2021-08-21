---
title: Attributo optimize
description: L'attributo \ optimize\ ACF viene usato per ottimizzare il livello di gradazione per il marshalling dei dati.
ms.assetid: d636d940-0550-417f-a21a-065bdeaeb5d9
keywords:
- ottimizzare l'attributo MIDL
topic_type:
- apiref
api_name:
- optimize
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7703a3539ff16c7f2dc78d51c62cfe05612dcb6e935bb5c5701f9a7b59a9f1d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119869571"
---
# <a name="optimize-attribute"></a>Attributo optimize

**\[ L'attributo \]** OPTIMIZE ACF viene usato per ottimizzare il livello di gradazione per il marshalling dei dati.

> [!Note]  
> Questa parola chiave è sostituita e non deve essere usata. Le compilazioni MIDL correnti devono usare [**/Oicf**](-oi.md)[**/robust.**](-robust.md)

 

``` syntax
optimize ("optimization-options")
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*opzioni di ottimizzazione* 
</dt> <dd>

Specifica il metodo di marshalling dei dati. Usare "s" per il marshalling in modalità mista o "i" per il marshalling interpretato.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa versione di RPC fornisce due metodi per il marshalling dei dati: in modalità mista ("s") e interpretata ("i"). Questi metodi corrispondono alle opzioni della riga di comando [**/Os**](-os.md) e [**/Oi.**](-oi.md) Il metodo interpretato effettua il marshalling dei dati completamente offline. Anche se ciò può ridurre notevolmente le dimensioni dello stub, le prestazioni possono essere influenzate.

Se le prestazioni sono un problema, il metodo in modalità mista può essere l'approccio migliore. La modalità mista consente al compilatore MIDL di determinare tra quali dati verrà effettuato il marshalling inline e quali verranno sottoposti a marshalling da una chiamata a una libreria a collegamento dinamico offline. Se molte procedure usano gli stessi tipi di dati, è possibile chiamare ripetutamente una singola routine per effettuare il marshalling dei dati. In questo modo, i dati più adatti per il marshalling inline vengono elaborati inline mentre altri dati possono essere sottoposti a marshalling offline in modo più efficiente.

Si noti che **\[ l'attributo optimize \]** può essere usato come attributo di interfaccia o come attributo dell'operazione. Se viene usato come attributo di interfaccia, imposta il valore predefinito per l'intera interfaccia, eseguendo l'override delle opzioni della riga di comando. Se, tuttavia, viene usato come attributo dell'operazione, influisce solo su tale operazione, eseguendo l'override delle opzioni della riga di comando e dell'interfaccia predefinita.

## <a name="examples"></a>Esempi

``` syntax
optimize ("s") HRESULT FasterProcedure(...); 
optimize ("i") HRESULT SmallerProcedure(...);
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[File di configurazione dell'applicazione (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**/oi**](-oi.md)
</dt> <dt>

[**/Os**](-os.md)
</dt> <dt>

[**/robust**](-robust.md)
</dt> </dl>

 

 




