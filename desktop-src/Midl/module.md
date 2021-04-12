---
title: attributo module
description: L'istruzione Module definisce un gruppo di funzioni, in genere un set di punti di ingresso della DLL.
ms.assetid: 4dec207f-98bc-4784-a3c9-506ffe7523fe
keywords:
- attributo del modulo MIDL
topic_type:
- apiref
api_name:
- module
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1eb310c3e126caf9b25b8c015b840aea11791d8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104337134"
---
# <a name="module-attribute"></a>attributo module

L'istruzione **Module** definisce un gruppo di funzioni, in genere un set di punti di ingresso della dll.

``` syntax
[
    attributes
]
module modulename 
{
    elementlist
};
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*attributes* 
</dt> <dd>

Gli \[ attributi [**UUID**](uuid.md) \] , \[ [**Version**](version.md) \] , \[ [**helpstring**](helpstring.md) \] , \[ [**HelpContext**](helpcontext.md) \] , \[ [**Hidden**](hidden.md) \] e \[ [**dllname**](dllname-str-.md) \] sono accettati prima di un'istruzione **Module** . Per ulteriori informazioni sugli attributi accettati prima della definizione di un modulo, vedere [descrizioni](/previous-versions/windows/desktop/automat/attribute-descriptions)degli attributi nel manuale di automazione OLE. L' \[ attributo **dllname** \] è obbligatorio. Se l' \[  \] attributo uuid viene omesso, il modulo non viene specificato in modo univoco nel sistema.

</dd> <dt>

*moduleName* 
</dt> <dd>

Nome del modulo.

</dd> <dt>

*elemento element* 
</dt> <dd>

Elenco di definizioni di costanti e prototipi di funzione per ogni funzione nella DLL. Un numero qualsiasi di definizioni di funzione può essere visualizzato nell'elenco di funzioni. Una funzione nell'elenco di funzioni ha il formato seguente:

\[*attributi* \] di *returnType* \[ funcname della convenzione di *chiamata* \] (*params*);

\[*attributi* \] di [**const**](const.md) constantType *const*  =  *ConstVal*;

\[ [](helpstring.md) \] \[ [](helpcontext.md) \] Per un [**const**](const.md)sono accettati solo gli attributi helpstring e HelpContext.

Gli attributi seguenti sono accettati in una funzione in un modulo: \[ [**helpstring**](helpstring.md) \] , \[ [**HelpContext**](helpcontext.md) \] , \[ [**String**](string.md) \] , \[ [**entry**](entry.md) \] , \[ [**propget**](propget.md) \] , \[ [**propput**](propput.md) \] , \[ [**propputref**](propputref.md) \] e \[ [**vararg**](vararg.md) \] . Se \[  \] viene specificato vararg, l'ultimo parametro deve essere una matrice sicura di tipo **Variant** .

La convenzione di chiamata facoltativa può essere uno dei \_ \_ Pascal/ \_ Pascal/Pascal, \_ \_ cdecl/ \_ cdecl/cdecl o \_ \_ stdcall/ \_ stdcall/stdcall. Il *tipo della convenzione di chiamata paramName* può includere fino a due caratteri di sottolineatura iniziali.

L'elenco di parametri è un elenco delimitato da virgole di:

\[*attributi*\]

Il tipo può essere qualsiasi tipo dichiarato in precedenza o tipo incorporato, un puntatore a qualsiasi tipo o un puntatore a un tipo incorporato. Gli attributi nei parametri sono:

\[[**in**](in.md) \] , \[ [**out**](out-idl.md) \] , \[ [**facoltativo**](optional.md) \] .

Se \[ [](optional.md) \] si utilizza facoltativo, i tipi di tali parametri devono essere **Variant** o **Variant** \* .

</dd> </dl>

## <a name="remarks"></a>Commenti

L'output del file di intestazione (. h) per i moduli è costituito da una serie di prototipi di funzione. La parola chiave **Module** e le parentesi circostanti vengono rimosse dall'output del file di intestazione (. h), ma prima dei prototipi viene inserito un commento (// **Module** *ModuleName*). La parola chiave **extern** viene inserita prima delle dichiarazioni.

## <a name="examples"></a>Esempi

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC), 
    helpstring("This is not GDI.EXE"), 
    helpcontext(190), 
    dllname("MATH.DLL")
] 
module somemodule
{ 
    [helpstring("Color for the frame")] 
            unsigned long const COLOR_FRAME = 0xH80000006; 
    [helpstring("Not a rectangle but a square"), 
     entry(1)] 
            pascal double square([in] double x); 
};
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[**const**](const.md)
</dt> <dt>

[Contenuto di una libreria dei tipi](/previous-versions/windows/desktop/automat/contents-of-a-type-library)
</dt> <dt>

[**DllName**](dllname-str-.md)
</dt> <dt>

[**voce**](entry.md)
</dt> <dt>

[Generazione di una libreria dei tipi con MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**helpcontext**](helpcontext.md)
</dt> <dt>

[**helpstring**](helpstring.md)
</dt> <dt>

[**nascosto**](hidden.md)
</dt> <dt>

[Sintassi del file di FAD](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**propget**](propget.md)
</dt> <dt>

[**propput**](propput.md)
</dt> <dt>

[**propputref**](propputref.md)
</dt> <dt>

[**string**](string.md)
</dt> <dt>

[**TYPEFLAGS**](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[**uuid**](uuid.md)
</dt> <dt>

[**vararg**](vararg.md)
</dt> <dt>

[**Versione**](version.md)
</dt> </dl>

 

 