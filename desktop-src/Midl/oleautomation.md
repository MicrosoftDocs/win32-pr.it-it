---
title: oleautomation (attributo)
description: Attributo MIDL oleautomation e compatibilità con l'automazione.
ms.assetid: 4a1c9a02-d637-4595-87b3-5fe903149357
keywords:
- attributo MIDL di oleautomation
topic_type:
- apiref
api_name:
- oleautomation
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b827aba4cb0871f7130e658299c6d8836557a156
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104046725"
---
# <a name="oleautomation-attribute"></a>oleautomation (attributo)

L'attributo **oleautomation** indica che un'interfaccia è compatibile con l'automazione.

``` syntax
[ 
    oleautomation, 
    uuid(string-uuid)
    [ , interface-attribute-list] 
] 
interface interface-name : base-interface
{
    ...
}
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*stringa-UUID* 
</dt> <dd>

Specifica una stringa UUID generata dall'utilità uuidgen.

</dd> <dt>

*Interface-Attribute-List* 
</dt> <dd>

Specifica altri attributi che si applicano all'interfaccia nel suo complesso.

</dd> <dt>

*Nome interfaccia* 
</dt> <dd>

Specifica il nome dell'interfaccia.

</dd> <dt>

*interfaccia di base* 
</dt> <dd>

Specifica il nome di un'interfaccia di automazione dalla quale questa interfaccia derivata eredita le funzioni membro, i codici di stato e gli attributi di interfaccia. Tutte le interfacce di automazione sono derivate da [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) o [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch).

</dd> </dl>

## <a name="remarks"></a>Commenti

I parametri e i tipi restituiti specificati per i membri di un'interfaccia **\[ oleautomation \]** devono essere compatibili con l'automazione, come elencato nella tabella seguente.



| Tipo                                            | Descrizione                                                                                                                                                                                                   |
|-------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **boolean**                                     | Elemento dati il cui valore può essere \_ true o Variant \_ false. Le dimensioni corrispondono alla variabile \_ bool.                                                                                                     |
| **unsigned char**                               | elemento di dati senza segno a 8 bit.                                                                                                                                                                                     |
| **double**                                      | numero a virgola mobile IEEE a 64 bit.                                                                                                                                                                            |
| **float**                                       | numero a virgola mobile IEEE a 32 bit.                                                                                                                                                                            |
| **int**                                         | Signed Integer, le cui dimensioni sono dipendenti dal sistema. Nelle piattaforme a 32 bit, MIDL considera [**int**](int.md) come intero con segno a 32 bit.                                                                               |
| **long**                                        | Intero con segno a 32 bit.                                                                                                                                                                                        |
| **short**                                       | intero con segno a 16 bit.                                                                                                                                                                                        |
| **BSTR**                                        | Stringa con prefisso length, come descritto nell'argomento di automazione [BSTR](/previous-versions/windows/desktop/automat/bstr).                                                                                                    |
| **CURRENCY**                                    | numero a virgola mobile fisso a 8 byte.                                                                                                                                                                          |
| **DATE**                                        | 64 bit, numero frazionario di giorni a virgola mobile a partire dal 30 dicembre 1899.                                                                                                                                     |
| **SCODE**                                       | Per i sistemi a 16 bit: tipo di errore predefinito corrispondente all'errore VT \_ .                                                                                                                                         |
| **Typedef (enumerazione** )  *Enum*                      | Signed Integer, le cui dimensioni sono dipendenti dal sistema.                                                                                                                                                               |
| **Interfaccia IDispatch \***                      | Puntatore all'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) (invio del VT \_ ).                                                                                                                |
| **IUnknown interfaccia \***                       | Puntatore a un'interfaccia che non deriva da [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) (VT \_ sconosciuto). Qualsiasi interfaccia OLE può essere rappresentata dalla relativa interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . |
| **interfaccia dispatch**  *TypeName \**                | Puntatore a un'interfaccia derivata da [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) (invio di un VT \_ ).                                                                                                    |
| **Coclasse**  *TypeName \**                      | Puntatore a un nome di coclasse (VT \_ sconosciuto).                                                                                                                                                                      |
| **\[ \] interfaccia oleautomation**.  *TypeName \** | Puntatore a un'interfaccia che deriva da [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown).                                                                                                                                      |
| **SAFEARRAY**(*typeName*)                       | *TypeName* è uno dei tipi precedenti. Matrice di questi tipi.                                                                                                                                                   |
| **TypeName \***                                 | *TypeName* è uno dei tipi precedenti. Puntatore a un tipo.                                                                                                                                                      |
| **Decimale**                                     | intero binario senza segno a 96 bit ridimensionato in base a una potenza variabile di 10. Tipo di dati Decimal che fornisce una dimensione e una scala per un numero (come nelle coordinate).                                                       |



 

Un parametro è compatibile con l'automazione se il tipo è un tipo compatibile con l'automazione, un puntatore a un tipo compatibile con l'automazione o un SAFEARRAY di un tipo compatibile con l'automazione.

Un tipo restituito è compatibile con l'automazione se il tipo è HRESULT, SCODE o [**void**](void.md). Tuttavia, MIDL richiede che i metodi di interfaccia restituiscano HRESULT o SCODE. Restituendo **void** viene generato un errore del compilatore.

Un membro è compatibile con l'automazione se il tipo restituito e tutti i relativi parametri sono compatibili con l'automazione.

Un'interfaccia è compatibile con l'automazione se è derivata da [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) o [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), ha l'attributo **\[ oleautomation \]** e tutte le relative voci VTBL sono compatibili con l'automazione. Per le piattaforme a 32 bit, la convenzione di chiamata per tutti i metodi nell'interfaccia deve essere STDCALL. Per i sistemi a 16 bit, tutti i metodi devono avere la convenzione di chiamata CDECL.

Ogni [**interfaccia dispatch**](dispinterface.md) è implicitamente compatibile con l'automazione. Pertanto, non è consigliabile usare l'attributo **\[ \] oleautomation** in **Dispatch**.

L'attributo **\[ \] oleautomation** non è disponibile quando si esegue la compilazione con l'opzione [**/OSF**](-osf.md) del compilatore MIDL.

### <a name="flags"></a>Flags

\_FOLEAUTOMATION TYPEFLAG

## <a name="examples"></a>Esempi

``` syntax
library Hello
{
    importlib("stdole32.tlb");
    [
        uuid(12345678-1234-1234-1234-123456789ABC),
        helpstring("Application object for the Hello application."),
        oleautomation,
        dual
    ]
    interface IHello : IDispatch
    {
        // Interface definition statements.
    }

    // Other library definition statements.
}
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[File di definizione dell'interfaccia (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[Generazione di una libreria dei tipi con MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[Esempio di file di FAD](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Sintassi del file di FAD](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[**uuid**](uuid.md)
</dt> </dl>

 

 