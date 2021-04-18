---
title: Optimize (attributo)
description: L'attributo \ Optimize \ ACF viene usato per ottimizzare il livello di gradazione per i dati di marshalling.
ms.assetid: d636d940-0550-417f-a21a-065bdeaeb5d9
keywords:
- Optimize attribute MIDL
topic_type:
- apiref
api_name:
- optimize
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6025c40465ecf2e8fe7a33dcda50ece07d34b9d
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "106299073"
---
# <a name="optimize-attribute"></a>Optimize (attributo)

L'attributo **\[ optimize \]** ACF viene usato per ottimizzare il livello di gradazione per i dati di marshalling.

> [!Note]  
> Questa parola chiave è superceeded e non deve essere usata. Le compilazioni MIDL correnti devono invece usare [**/Oicf**](-oi.md)[**/robust**](-robust.md) .

 

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

Questa versione di RPC fornisce due metodi per il marshalling dei dati: in modalità mista ("s") e interpretati ("i"). Questi metodi corrispondono alle opzioni della riga di comando [**/OS**](-os.md) e [**/OI**](-oi.md) . Il metodo interpretato esegue il marshalling dei dati completamente offline. Sebbene ciò possa ridurre notevolmente le dimensioni dello stub, le prestazioni possono essere influenzate.

Se le prestazioni sono un problema, il metodo in modalità mista può essere l'approccio migliore. La modalità mista consente al compilatore MIDL di determinare tra i dati di cui verrà eseguito il marshalling inline e di cui verrà effettuato il marshalling da una chiamata a una libreria a collegamento dinamico offline. Se molte procedure utilizzano gli stessi tipi di dati, è possibile chiamare ripetutamente una singola procedura per effettuare il marshalling dei dati. In questo modo, i dati più appropriati per il marshalling inline vengono elaborati inline mentre altri dati possono essere sottoposti a marshalling in modo più efficiente offline.

Si noti che l'attributo **\[ optimize \]** può essere utilizzato come attributo di interfaccia o come attributo Operation. Se viene usato come attributo di interfaccia, imposta il valore predefinito per l'intera interfaccia, eseguendo l'override delle opzioni della riga di comando. Se, tuttavia, viene utilizzato come attributo dell'operazione, influiscono solo su tale operazione, ignorando le opzioni della riga di comando e l'interfaccia predefinita.

## <a name="examples"></a>Esempi

``` syntax
optimize ("s") HRESULT FasterProcedure(...); 
optimize ("i") HRESULT SmallerProcedure(...);
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[File di configurazione dell'applicazione (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**/OI**](-oi.md)
</dt> <dt>

[**/OS**](-os.md)
</dt> <dt>

[**/Robust**](-robust.md)
</dt> </dl>

 

 




