---
title: dual (attributo)
description: L'attributo dual identifica un'interfaccia che espone proprietà e metodi tramite IDispatch e direttamente tramite VTBL.
ms.assetid: 1c214f10-57eb-4a05-99a8-a09770666a74
keywords:
- dual attribute MIDL
topic_type:
- apiref
api_name:
- dual
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1e1e9cd15c1b219d07518c9630880a5010226c96c63d57539ffb66fab3a6c02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118643095"
---
# <a name="dual-attribute"></a>dual (attributo)

**L'attributo dual** identifica un'interfaccia che espone proprietà e metodi tramite [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) e direttamente tramite VTBL.

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

*uuid-number* 
</dt> <dd>

Specifica un numero di identificazione universalmente univoco per l'interfaccia

</dd> <dt>

*optional-attribute-list* 
</dt> <dd>

Specifica un elenco di zero o più attributi MIDL aggiuntivi.

</dd> <dt>

*interface-name* 
</dt> <dd>

Nome dell'interfaccia a cui verrà **applicato l'attributo** duale.

</dd> </dl>

## <a name="remarks"></a>Commenti

Le interfacce identificate **dall'attributo dual** devono essere compatibili con Automazione ed essere derivate da [**IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) Questo attributo non è consentito nelle interfacce dispatch.

**L'attributo** dual crea un'interfaccia che è sia [**un'interfaccia IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) che un'Component Object Model (COM). Le prime sette voci del VTBL per un'interfaccia duale sono i sette membri di **IDispatch** e le voci rimanenti sono per l'accesso diretto ai membri dell'interfaccia duale. Tutti i parametri e i tipi restituiti specificati per i membri di un'interfaccia duale devono essere tipi compatibili con l'automazione.

Tutti i membri di un'interfaccia duale devono passare un HRESULT come valore restituito dalla funzione. I membri, ad esempio le funzioni di accesso alle proprietà, che devono restituire altri valori, devono specificare l'ultimo parametro come [**out**](out-idl.md), [**retval**](retval.md), che indica un parametro di output che restituisce il valore della funzione. Inoltre, i membri che devono supportare più impostazioni locali devono passare un [**parametro lcid.**](lcid.md)

Un'interfaccia duale offre sia la velocità dell'associazione VTBL diretta che la flessibilità [**dell'associazione IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) Per questo motivo, le interfacce duali sono consigliate quando possibile.

> [!Note]  
> Se l'applicazione accede ai dati dell'oggetto eseguendo il cast del puntatore *this* all'interno della chiamata di interfaccia, è necessario controllare i puntatori VTBL nell'oggetto rispetto ai puntatori VTBL per assicurarsi di essere connessi al proxy appropriato.

 

Se si specifica **dual** su un'interfaccia, l'interfaccia è compatibile con l'automazione e pertanto vengono impostati i flag TYPEFLAG \_ FDUAL e TYPEFLAG \_ PIÙAUTOMATION.

### <a name="flags"></a>Flags

TYPEFLAG \_ FDUAL, TYPEFLAG \_ LAEAUTOMATION

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

[**Interfaccia**](interface.md)
</dt> <dt>

[**Lcid**](lcid.md)
</dt> <dt>

[**oleautomation**](oleautomation.md)
</dt> <dt>

[Sintassi del file ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Esempio di file ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[**in uscita**](out-idl.md)
</dt> <dt>

[**retval**](retval.md)
</dt> </dl>

 

 