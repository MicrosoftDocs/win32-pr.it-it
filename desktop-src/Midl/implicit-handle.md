---
title: implicit_handle attributo
description: L'attributo ACF \ implicit handle\ specifica l'handle usato per le funzioni che non includono un \_ handle esplicito come parametro di routine.
ms.assetid: 09c17473-87b5-4fd6-beb9-3d9b7bc82d8c
keywords:
- implicit_handle attributo MIDL
topic_type:
- apiref
api_name:
- implicit_handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17c53ded4c7459be8f0c8eb98f3770d88ff88a9b7da20cb3482c1032a4f74e96
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013809"
---
# <a name="implicit_handle-attribute"></a>attributo \_ handle implicito

L'attributo ACF **\[ \_ dell'handle \] implicito** specifica l'handle usato per le funzioni che non includono un handle esplicito come parametro di routine.

``` syntax
implicit_handle(handle-type handle-name)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*handle-type* 
</dt> <dd>

Specifica il tipo di dati handle, ad esempio l'handle del tipo di base [**\_ t**](handle-t.md) o un tipo di handle definito dall'utente.

</dd> <dt>

*handle-name* 
</dt> <dd>

Specifica il nome dell'handle.

</dd> </dl>

## <a name="remarks"></a>Commenti

L'handle specificato **\[ dall'attributo \_ handle \] implicito** viene utilizzato in modi diversi a seconda della natura della procedura. Se la procedura è remota, l'handle verrà utilizzato come handle di associazione per la chiamata remota. L'handle implicito può essere usato anche per stabilire un'associazione iniziale per una funzione che usa un handle di contesto. Se la procedura è una procedura di serializzazione, l'handle viene utilizzato come handle di serializzazione che controlla l'operazione. Nel caso della serializzazione del tipo, l'handle viene utilizzato come handle di serializzazione per tutti i tipi serializzati.

**\[ \_ L'attributo \] handle implicito** specifica una variabile globale che contiene un handle usato da qualsiasi funzione che necessitano di handle impliciti.

Il tipo di handle di associazione implicito deve essere [**handle \_ t**](handle-t.md) (o un tipo basato **sull'handle \_ t**) o un tipo di handle definito dall'utente specificato con l'attributo [**handle.**](handle.md) L'handle di serializzazione implicita deve essere un tipo basato **sull'handle \_ t**.

Se il tipo di handle implicito non è definito nel file IDL o in qualsiasi file incluso e importato dal file IDL per il computer MIDL, è necessario specificare il file contenente la definizione del tipo di handle quando si compilano gli stub. Usare l'istruzione [**INCLUDE**](include.md) di ACF per includere il file contenente la definizione del tipo di handle.

**\[ \_ L'attributo \] handle implicito** può verificarsi al massimo una volta. **\[ \_ L'attributo \] handle implicito** può verificarsi solo se gli [**\[ attributi handle \_ automatico \]**](auto-handle.md) e [**\[ handle \_ \]**](explicit-handle.md) esplicito non si verificano.

## <a name="examples"></a>Esempi

``` syntax
/* ACF file */ 
[
    implicit_handle(handle_t hMyHandle)
] 
interface iface
{ 
    // Attribute configuration statements
}
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[File di configurazione dell'applicazione (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**handle \_ automatico**](auto-handle.md)
</dt> <dt>

[**handle \_ esplicito**](explicit-handle.md)
</dt> <dt>

[**handle \_ t**](handle-t.md)
</dt> <dt>

[**Includono**](include.md)
</dt> </dl>

 

 




