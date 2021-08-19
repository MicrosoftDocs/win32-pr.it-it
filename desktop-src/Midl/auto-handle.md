---
title: auto_handle attributo
description: L'attributo ACF \ auto handle\ indica al stub di stabilire automaticamente l'associazione per una funzione che non dispone di un parametro \_ di handle di associazione esplicito. Nota Questo attributo è obsoleto e non è più supportato.
ms.assetid: a402b933-f69b-4dfe-b0c5-b034d65d4a84
keywords:
- auto_handle attributo MIDL
topic_type:
- apiref
api_name:
- auto_handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e1f42a2fb643a2ce643437aad73b13c6e55d3462e92f9ce52ba208c6dc5cb68
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117807884"
---
# <a name="auto_handle-attribute"></a>attributo \_ di handle automatico

**\[ \_ L'attributo \]** ACF di gestione automatica indica al stub di stabilire automaticamente l'associazione per una funzione che non dispone di un parametro di handle di associazione esplicito.

> [!Note]  
> Questo attributo è obsoleto e non è più supportato. È consigliabile [**usare l'opzione /robust.**](-robust.md)

 

``` syntax
[ 
    auto_handle [, interface-attribute-list] 
] 
interface interface-name
{
    interface-definition
}
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*interface-attribute-list* 
</dt> <dd>

Specifica zero o più attributi che si applicano all'intera interfaccia, ad esempio [**code**](code.md) o [**nocode.**](nocode.md) Separare gli attributi dell'interfaccia con virgole.

</dd> <dt>

*interface-name* 
</dt> <dd>

Specifica il nome dell'interfaccia.

</dd> <dt>

*interface-definition* 
</dt> <dd>

Specifica le istruzioni IDL che formano la definizione dell'interfaccia.

</dd> </dl>

## <a name="remarks"></a>Commenti

**\[ \_ L'attributo \] handle** automatico viene visualizzato nell'intestazione dell'interfaccia di ACF. Viene visualizzato anche nell'intestazione dell'interfaccia del file IDL quando si specifica l'opzione del compilatore MIDL [**/app \_ config**](-app-config.md).

Quando il client chiama una funzione che usa l'associazione automatica e non esiste alcuna associazione a un server, lo stub stabilisce automaticamente l'associazione. L'associazione viene riutilizzata per le chiamate successive ad altre funzioni nell'interfaccia che usano l'associazione automatica. Il programma dell'applicazione client non deve dichiarare o eseguire alcuna elaborazione relativa all'handle di associazione.

Quando ACF non è presente o non include l'attributo [**\[ \_ handle \] implicito,**](implicit-handle.md) il compilatore MIDL usa l'handle **\[ \_ \]** automatico e genera un messaggio informativo. Il compilatore MIDL usa anche **\[ \_ l'handle automatico \]**, se necessario, per stabilire l'associazione iniziale per un handle di [**\[ \_ contesto \]**](context-handle.md).

**\[ L'attributo \_ handle \]** automatico può verificarsi solo se l'handle [**\[ \_ implicito o \]**](implicit-handle.md) l'attributo [**\[ \_ handle \]**](explicit-handle.md) esplicito non si verifica. **\[ L'attributo di \_ handle \]** automatico può essere presente al massimo nell'intestazione dell'interfaccia ACF o IDL.

> [!Note]  
> Non è possibile usare l'associazione automatica (con **\[ l'attributo \_ handle \]** automatico o per impostazione predefinita) se si elaborano dati tramite pipe.

 

## <a name="examples"></a>Esempi

``` syntax
[
    auto_handle
] 
interface MyInterface 
{ 
    /* Interface definition goes here*/
} 
[
    auto_handle, 
    code
] 
interface MyInterface
{ 
    /* Interface definition goes here*/
}
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[File di configurazione dell'applicazione (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**/app \_ config**](-app-config.md)
</dt> <dt>

[**Codice**](code.md)
</dt> <dt>

[**handle \_ esplicito**](explicit-handle.md)
</dt> <dt>

[**handle di \_ contesto**](context-handle.md)
</dt> <dt>

[**handle \_ implicito**](implicit-handle.md)
</dt> <dt>

[**nocode**](nocode.md)
</dt> </dl>

 

 




