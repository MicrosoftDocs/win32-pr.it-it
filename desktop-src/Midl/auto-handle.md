---
title: attributo auto_handle
description: L'attributo \ auto \_ handle \ ACF indica allo stub di stabilire automaticamente l'associazione per una funzione che non dispone di un parametro di handle di binding esplicito. Si noti che questo attributo è obsoleto e non è più supportato.
ms.assetid: a402b933-f69b-4dfe-b0c5-b034d65d4a84
keywords:
- attributo auto_handle MIDL
topic_type:
- apiref
api_name:
- auto_handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01e9a4c91fac8553867536f4f5a8c3094e0f0ff9
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104471910"
---
# <a name="auto_handle-attribute"></a>\_attributo handle automatico

L'attributo **\[ \_ gestione \] automatica** ACF indica allo stub di stabilire automaticamente l'associazione per una funzione che non dispone di un parametro di handle di binding esplicito.

> [!Note]  
> Questo attributo è obsoleto e non è più supportato. È consigliabile usare l'opzione [**/robust**](-robust.md) .

 

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

*Interface-Attribute-List* 
</dt> <dd>

Specifica zero o più attributi che si applicano all'interfaccia nel suo complesso, ad esempio [**Code**](code.md) o [**NoCode**](nocode.md). Separare gli attributi di interfaccia con virgole.

</dd> <dt>

*Nome interfaccia* 
</dt> <dd>

Specifica il nome dell'interfaccia.

</dd> <dt>

*interfaccia-definizione* 
</dt> <dd>

Specifica le istruzioni IDL che formano la definizione dell'interfaccia.

</dd> </dl>

## <a name="remarks"></a>Commenti

L'attributo **\[ \_ handle \] automatico** viene visualizzato nell'intestazione Interface di ACF. Viene inoltre visualizzato nell'intestazione di interfaccia del file IDL quando si specifica l'opzione del compilatore MIDL [**/app \_ config**](-app-config.md).

Quando il client chiama una funzione che utilizza il binding automatico e non esiste alcun binding a un server, lo stub stabilisce automaticamente l'associazione. L'associazione viene riutilizzata per le chiamate successive ad altre funzioni nell'interfaccia che utilizzano l'associazione automatica. Il programma dell'applicazione client non deve dichiarare né eseguire alcuna elaborazione relativa all'handle di associazione.

Quando ACF non è presente o non include l'attributo [**\[ \_ handle \] implicito**](implicit-handle.md) , il compilatore MIDL usa l' **\[ \_ handle \] automatico** e genera un messaggio informativo. Il compilatore MIDL usa anche l' **\[ \_ handle \] automatico**, se necessario, per stabilire l'associazione iniziale per un [**\[ \_ handle \] di contesto**](context-handle.md).

L'attributo **\[ \_ handle \] automatico** può verificarsi solo se l' [**\[ \_ handle \] implicito**](implicit-handle.md) o l'attributo [**\[ \_ handle \] esplicito**](explicit-handle.md) non si verifica. L'attributo **\[ \_ handle \] automatico** può essere presente all'interno dell'intestazione dell'interfaccia ACF o IDL al massimo una volta.

> [!Note]  
> Non è possibile usare l'associazione automatica (con l'attributo **\[ \_ handle \] automatico** o per impostazione predefinita) se si elaborano i dati attraverso le pipe.

 

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

[**configurazione di/app \_**](-app-config.md)
</dt> <dt>

[**codice**](code.md)
</dt> <dt>

[**handle esplicito \_**](explicit-handle.md)
</dt> <dt>

[**handle di contesto \_**](context-handle.md)
</dt> <dt>

[**handle implicito \_**](implicit-handle.md)
</dt> <dt>

[**NoCode**](nocode.md)
</dt> </dl>

 

 




