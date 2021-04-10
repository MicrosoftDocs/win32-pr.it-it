---
title: dual (attributo)
description: L'attributo dual identifica un'interfaccia che espone proprietà e metodi tramite IDispatch e direttamente tramite il VTBL.
ms.assetid: 1c214f10-57eb-4a05-99a8-a09770666a74
keywords:
- MIDL attributo doppio
topic_type:
- apiref
api_name:
- dual
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39a9e44de464f58fd1ffc0606551b9a0203ae9e9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103963064"
---
# <a name="dual-attribute"></a>dual (attributo)

L'attributo **Dual** identifica un'interfaccia che espone proprietà e metodi tramite [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) e direttamente tramite il VTBL.

``` syntax
[
    uuid(uuid-number), 
    oleautomation,
    dual 
  [ , optional-attribute-list]
]
interface interface-name
{
    . . .
};
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*UUID-numero* 
</dt> <dd>

Specifica un numero di identificazione univoco universale per l'interfaccia

</dd> <dt>

*facoltativo-Attribute-List* 
</dt> <dd>

Specifica un elenco di zero o più attributi MIDL aggiuntivi.

</dd> <dt>

*Nome interfaccia* 
</dt> <dd>

Nome dell'interfaccia a cui verrà applicato l'attributo **doppio** .

</dd> </dl>

## <a name="remarks"></a>Commenti

Le interfacce identificate dall'attributo **duale** devono essere compatibili con l'automazione ed essere derivate da [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch). Questo attributo non è consentito in dispinterfaces.

L'attributo **duale** crea un'interfaccia che è sia un'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) che un'interfaccia Component Object Model (com). Le prime sette voci di VTBL per un'interfaccia duale sono i sette membri di **IDispatch** e le voci rimanenti sono per l'accesso diretto ai membri dell'interfaccia duale. Tutti i parametri e i tipi restituiti specificati per i membri di un'interfaccia duale devono essere tipi compatibili con l'automazione.

Tutti i membri di un'interfaccia duale devono passare un HRESULT come valore restituito della funzione. I membri, ad esempio le funzioni di accesso alle proprietà, che devono restituire altri valori, devono specificare l'ultimo parametro [**out**](out-idl.md), [**retval**](retval.md), che indica un parametro di output che restituisce il valore della funzione. Inoltre, i membri che devono supportare più impostazioni locali devono passare un parametro [**LCID**](lcid.md) .

Una doppia interfaccia fornisce sia per la velocità di associazione diretta di VTBL sia per la flessibilità del binding [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . Per questo motivo, le interfacce duali sono consigliate quando possibile.

> [!Note]  
> Se l'applicazione accede ai dati degli oggetti eseguendo il cast del puntatore *this* all'interno della chiamata di interfaccia, è consigliabile controllare i puntatori VTBL nell'oggetto in base ai puntatori VTBL per assicurarsi di essere connessi al proxy appropriato.

 

Se si specifica **Dual** su un'interfaccia, l'interfaccia è compatibile con l'automazione e pertanto \_ vengono impostati i flag TYPEFLAG FDUAL e TypeFlag \_ FOLEAUTOMATION.

### <a name="flags"></a>Flags

TYPEFLAG \_ FDUAL, TypeFlag \_ FOLEAUTOMATION

## <a name="examples"></a>Esempi

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676), 
    oleautomation, dual
]
interface IHello : IDispatch
{
    //Diverse properties and methods defined here.
};
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[Generazione di una libreria dei tipi con MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**interfaccia**](interface.md)
</dt> <dt>

[**LCID**](lcid.md)
</dt> <dt>

[**oleautomation**](oleautomation.md)
</dt> <dt>

[Sintassi del file di FAD](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Esempio di file di FAD](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[**out**](out-idl.md)
</dt> <dt>

[**retval**](retval.md)
</dt> </dl>

 

 