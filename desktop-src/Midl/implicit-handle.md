---
title: attributo implicit_handle
description: L'attributo \ Implicit \_ handle \ ACF specifica l'handle usato per le funzioni che non includono un handle esplicito come parametro di procedura.
ms.assetid: 09c17473-87b5-4fd6-beb9-3d9b7bc82d8c
keywords:
- attributo implicit_handle MIDL
topic_type:
- apiref
api_name:
- implicit_handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22f410fa048a27e1f7626690e6308de4c1a31c2a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "103857229"
---
# <a name="implicit_handle-attribute"></a>\_attributo handle implicito

L'attributo ACF dell' **\[ \_ handle \] implicito** specifica l'handle usato per le funzioni che non includono un handle esplicito come parametro di procedura.

``` syntax
implicit_handle(handle-type handle-name)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*tipo di handle* 
</dt> <dd>

Specifica il tipo di dati dell'handle, ad esempio l' [**handle \_**](handle-t.md) del tipo di base t o un tipo di handle definito dall'utente.

</dd> <dt>

*nome handle* 
</dt> <dd>

Specifica il nome dell'handle.

</dd> </dl>

## <a name="remarks"></a>Commenti

L'handle specificato dall'attributo **\[ \_ handle \] implicito** viene utilizzato in modi diversi a seconda della natura della routine. Se la procedura è remota, l'handle verrà usato come handle di binding per la chiamata remota. L'handle implicito può essere usato anche per stabilire un'associazione iniziale per una funzione che usa un handle di contesto. Se la procedura è una procedura di serializzazione, l'handle viene utilizzato come un handle di serializzazione che controlla l'operazione. Nel caso della serializzazione del tipo, l'handle viene utilizzato come handle di serializzazione per tutti i tipi serializzati.

L'attributo **\[ \_ handle \] implicito** specifica una variabile globale che contiene un handle utilizzato da qualsiasi funzione che necessita di handle impliciti.

Il tipo di handle di binding implicito deve essere [**handle \_ t**](handle-t.md) (o un tipo basato su **handle \_ t**) o un tipo di handle definito dall'utente specificato con l'attributo [**handle**](handle.md) . L'handle di serializzazione implicita deve essere un tipo basato su **handle \_ t**.

Se il tipo di handle implicito non è definito nel file IDL o nei file inclusi e importati dal file IDL per il computer MIDL, è necessario fornire il file contenente la definizione del tipo di handle quando si compilano gli stub. Usare l'istruzione di [**inclusione**](include.md) di ACF per includere il file contenente la definizione del tipo di handle.

L'attributo **\[ \_ handle \] implicito** può essere presente al massimo una volta. L'attributo **\[ \_ handle \] implicito** può verificarsi solo [**\[ \_ \]**](auto-handle.md) se gli attributi handle automatico e [**\[ \_ handle \] esplicito**](explicit-handle.md) non vengono eseguiti.

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

[**\_handle automatico**](auto-handle.md)
</dt> <dt>

[**handle esplicito \_**](explicit-handle.md)
</dt> <dt>

[**handle \_ t**](handle-t.md)
</dt> <dt>

[**includere**](include.md)
</dt> </dl>

 

 




