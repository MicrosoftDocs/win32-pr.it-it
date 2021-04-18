---
title: attributo explicit_handle
description: L'attributo \ Explicit \_ handle \ ACF specifica che ogni routine ha, come primo parametro, un handle primitivo, ad esempio un tipo di handle \_ t.
ms.assetid: c95d005e-dcc7-4d83-885d-91c0773c0ed8
keywords:
- attributo explicit_handle MIDL
topic_type:
- apiref
api_name:
- explicit_handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed4fa677f1bb5a3414e6cf6dc761b83414c2d68b
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "106299086"
---
# <a name="explicit_handle-attribute"></a>\_attributo handle esplicito

L' \[ attributo di **\_ handle ACF esplicito** \] specifica che ogni routine ha come primo parametro un handle primitivo, ad esempio un tipo di [**handle \_ t**](handle-t.md) .

``` syntax
[
    explicit_handle
] 
interface interface-name
{
    ...
}
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*Nome interfaccia* 
</dt> <dd>

Specifica il nome dell'interfaccia.

</dd> </dl>

## <a name="remarks"></a>Commenti

Quando si utilizza l'attributo **\[ \_ handle \] esplicito** , ogni routine dispone di un handle primitivo come primo parametro anche se il file IDL non contiene questo handle nell'elenco dei parametri. I prototipi emessi per il file di intestazione e le routine stub contengono il parametro aggiuntivo e tale parametro viene usato come handle per indirizzare la chiamata remota.

L'attributo **\[ \_ handle \] esplicito** influiscono sia sulle procedure remote sia sulle procedure di serializzazione. Per la serializzazione del tipo, le routine di supporto vengono generate con il parametro iniziale come handle esplicito (serializzazione). Se non viene utilizzato l'attributo **\[ \_ handle \] esplicito** , l'applicazione può comunque specificare che un'operazione dispone di un handle esplicito (associazione o serializzazione) che indirizza la chiamata. A tale scopo, al file IDL viene fornito un prototipo con un argomento contenente un tipo di handle. Si noti che in modalità predefinita, un argomento che non viene visualizzato per primo può essere usato anche come handle che indirizza la chiamata.

Pertanto, mentre l'attributo **\[ \_ handle \] esplicito** è un modo per fornire al prototipo IDL un attributo di **\[ \_ handle \] esplicito** primitivo, non richiede necessariamente una modifica al file IDL. In modalità [**/OSF**](-osf.md) solo il primo argomento può essere utilizzato come tipo di handle esplicito.

L'attributo **\[ \_ handle \] esplicito** può essere utilizzato come attributo di interfaccia o attributo Operation. Come attributo di interfaccia, influiscono su tutte le operazioni nell'interfaccia e su tutti i tipi che richiedono il supporto della serializzazione. Se, tuttavia, viene utilizzato come attributo dell'operazione, influiscono solo su tale operazione specifica. Se un metodo contiene uno o più \[ \] handle di contesto, l'handle \[ di contesto più a sinistra \] viene usato come handle di associazione e non viene creato alcun handle esplicito aggiuntivo.

## <a name="examples"></a>Esempi

``` syntax
/* ACF File */ 
[
    explicit_handle
] 
interface iface
{ 
    // Interface definition statements.
};
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[File di configurazione dell'applicazione (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**\_handle automatico**](auto-handle.md)
</dt> <dt>

[**handle implicito \_**](implicit-handle.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> </dl>

 

 




