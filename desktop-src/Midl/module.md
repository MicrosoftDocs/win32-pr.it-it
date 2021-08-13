---
title: Attributo module
description: L'istruzione module definisce un gruppo di funzioni, in genere un set di punti di ingresso DLL.
ms.assetid: 4dec207f-98bc-4784-a3c9-506ffe7523fe
keywords:
- Attributo module MIDL
topic_type:
- apiref
api_name:
- module
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a83528a1ec632fcf2309438e6228220544a32408b310ea90260b8bcfda3cb6f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118642809"
---
# <a name="module-attribute"></a>Attributo module

**L'istruzione** module definisce un gruppo di funzioni, in genere un set di punti di ingresso DLL.

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

Gli \[ [**attributi uuid**](uuid.md) \] , \[ [**version**](version.md) \] , \[ [**helpstring**](helpstring.md), \] \[ [**helpcontext**](helpcontext.md), \] \[ [**hidden**](hidden.md) \] e \[ [**dllname**](dllname-str-.md) vengono \] accettati prima di un'istruzione **module.** Per [altre informazioni sugli](/previous-versions/windows/desktop/automat/attribute-descriptions)attributi accettati prima della definizione di un modulo, vedere Descrizione degli attributi nel libro Automazione OLE. \[ **L'attributo dllname** \] è obbligatorio. Se \[ **l'attributo uuid** viene omesso, il modulo non viene specificato in modo \] univoco nel sistema.

</dd> <dt>

*Modulename* 
</dt> <dd>

Nome del modulo.

</dd> <dt>

*elementlist* 
</dt> <dd>

Elenco di definizioni di costanti e prototipi di funzione per ogni funzione nella DLL. Nell'elenco delle funzioni può essere visualizzato un numero qualsiasi di definizioni di funzione. Una funzione nell'elenco di funzioni ha il formato seguente:

\[*attributi* \] *returntype* \[ *convenzione di chiamata funcname* \] (*params*);

\[*attributi* \] [**const**](const.md) constanttype *constname*  =  *constval*;

Per un oggetto const vengono accettati solo gli attributi \[ [](helpstring.md) \] \[ helpstring e [**helpcontext.**](helpcontext.md) \] [](const.md)

Gli attributi seguenti vengono accettati in una funzione in un modulo: \[ [**helpstring**](helpstring.md) \] , \[ [**helpcontext**](helpcontext.md), \] \[ [**string**](string.md), \] \[ [**entry**](entry.md), \] \[ [**propget**](propget.md), \] \[ [**propput**](propput.md), \] \[ [**propputref**](propputref.md)e \] \[ [**vararg**](vararg.md) \] . Se \[ **si specifica vararg,** \] l'ultimo parametro deve essere una matrice sicura di **tipo VARIANT.**

La convenzione di chiamata facoltativa può essere \_ \_ \_ pascal/pascal, \_ \_ cdecl/cdecl/cdecl o \_ \_ \_ stdcall/stdcall/stdcall. \_ Il tipo di convenzione di chiamata *paramname* può includere fino a due caratteri di sottolineatura iniziali.

L'elenco di parametri è un elenco delimitato da virgole di:

\[*Attributi*\]

Il tipo può essere qualsiasi tipo dichiarato in precedenza o predefinito, un puntatore a qualsiasi tipo o un puntatore a un tipo predefinito. Gli attributi nei parametri sono:

\[[**in**](in.md) \] , \[ [**out**](out-idl.md) \] , \[ [**facoltativo.**](optional.md) \]

Se \[ [**si**](optional.md) \] usa facoltativo, i tipi di tali parametri devono essere **VARIANT** o **VARIANT.** \*

</dd> </dl>

## <a name="remarks"></a>Commenti

L'output del file di intestazione (con estensione h) per i moduli è una serie di prototipi di funzione. La parola chiave **module** e le parentesi quadre racchiuse vengono rimosso dall'output del file di intestazione (con estensione h), ma prima dei prototipi viene inserito un commento (// **module** *modulename).* La parola **chiave extern** viene inserita prima delle dichiarazioni.

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

[**Dllname**](dllname-str-.md)
</dt> <dt>

[**Voce**](entry.md)
</dt> <dt>

[Generazione di una libreria dei tipi con MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**helpcontext**](helpcontext.md)
</dt> <dt>

[**helpstring**](helpstring.md)
</dt> <dt>

[**Nascosto**](hidden.md)
</dt> <dt>

[Sintassi del file ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
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

[**Uuid**](uuid.md)
</dt> <dt>

[**vararg**](vararg.md)
</dt> <dt>

[**Versione**](version.md)
</dt> </dl>

 

 