---
title: public (attributo)
description: L'attributo \ Public \ include un alias dichiarato con la parola chiave typedef nella libreria dei tipi.
ms.assetid: d4e90165-8b0d-47bb-998d-e515226be935
keywords:
- MIDL attributo pubblico
topic_type:
- apiref
api_name:
- public
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8451ddf77b5074dbea609bfed144340dc877c00
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299634"
---
# <a name="public-attribute"></a>public (attributo)

L'attributo **\[ \] public** include un alias dichiarato con la parola chiave [**typedef**](typedef.md) nella libreria dei tipi.

``` syntax
typedef [public] data-type identifier;
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*tipo di dati* 
</dt> <dd>

Tipo di dati per il quale l'identificatore sarà un alias.

</dd> <dt>

*identifier* 
</dt> <dd>

Un altro nome in base al quale il *tipo di dati* sarà noto nel software.

</dd> </dl>

## <a name="remarks"></a>Commenti

Per impostazione predefinita, un alias dichiarato con [**typedef**](typedef.md) e privo di altri attributi viene considerato come **\# definito** e non è incluso nella libreria dei tipi. L'utilizzo dell'attributo **\[ public \]** garantisce che l'alias diventi parte della libreria dei tipi.

> [!Note]  
> Per il compilatore MIDL è necessario applicare in modo esplicito l'attributo **\[ public \]** a ogni typedef che si desidera public.

 

## <a name="examples"></a>Esempi

``` syntax
typedef [public] long MEMBERID;
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[Generazione di una libreria dei tipi con MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[Esempio di file di FAD](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[**interfaccia**](interface.md)
</dt> <dt>

[Sintassi del file di FAD](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**typedef**](typedef.md)
</dt> </dl>

 

 