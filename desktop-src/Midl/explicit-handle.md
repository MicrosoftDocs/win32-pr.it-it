---
title: explicit_handle attributo
description: L'attributo ACF \ explicit handle\ specifica che ogni routine ha, come primo parametro, un handle primitivo, ad esempio \_ un tipo handle \_ t.
ms.assetid: c95d005e-dcc7-4d83-885d-91c0773c0ed8
keywords:
- explicit_handle attributo MIDL
topic_type:
- apiref
api_name:
- explicit_handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13b50aa69c43e27b4797f6619b4efa14b90f16dd2b4bee45df2db6b708e58f66
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013919"
---
# <a name="explicit_handle-attribute"></a>attributo \_ handle esplicito

L'attributo ACF dell'handle esplicito specifica che ogni routine ha, come primo parametro, un handle primitivo, ad esempio un tipo handle \[ **\_** \] [**\_ t.**](handle-t.md)

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

*interface-name* 
</dt> <dd>

Specifica il nome dell'interfaccia.

</dd> </dl>

## <a name="remarks"></a>Commenti

Quando si usa **\[ l'attributo \_ handle \]** esplicito, ogni routine dispone di un handle primitivo come primo parametro anche se il file IDL non contiene questo handle nel relativo elenco di parametri. I prototipi generati nel file di intestazione e nelle routine stub contengono il parametro aggiuntivo e tale parametro viene usato come handle per indirizzare la chiamata remota.

**\[ L'attributo handle \_ esplicito \]** influisce sia sulle procedure remote che sulle procedure di serializzazione. Per la serializzazione dei tipi, le routine di supporto vengono generate con il parametro iniziale come handle esplicito (serializzazione). Se **\[ \_ l'attributo handle \]** esplicito non viene usato, l'applicazione può comunque specificare che un'operazione dispone di un handle esplicito (associazione o serializzazione) che indirizza la chiamata. A tale scopo, al file IDL viene fornito un prototipo con un argomento contenente un tipo di handle. Si noti che in modalità predefinita, un argomento che non viene visualizzato per primo può essere usato anche come handle che indirizza la chiamata.

Pertanto, anche se l'attributo **\[ \_ handle \]** esplicito è un modo per fornire al prototipo IDL un attributo **\[ \_ handle \]** esplicito primitivo, non richiede necessariamente una modifica al file IDL. In [**modalità /osf**](-osf.md) solo il primo argomento può essere usato come tipo di handle esplicito.

**\[ \_ L'attributo \] handle** esplicito può essere usato come attributo di interfaccia o attributo dell'operazione. Come attributo di interfaccia, influisce su tutte le operazioni nell'interfaccia e su tutti i tipi che richiedono il supporto della serializzazione. Se, tuttavia, viene usato come attributo dell'operazione, influisce solo su tale operazione specifica. Se un metodo contiene uno o più handle di contesto, come handle di associazione viene utilizzato l'handle più a sinistra nel contesto e non viene \[ \] creato alcun handle \[ \] esplicito aggiuntivo.

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

[**handle \_ automatico**](auto-handle.md)
</dt> <dt>

[**handle \_ implicito**](implicit-handle.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> </dl>

 

 




