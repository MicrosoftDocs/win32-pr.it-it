---
title: object (attributo)
description: L'attributo di interfaccia \object\ identifica un'interfaccia COM.
ms.assetid: 51e34ef3-eea7-45f4-b961-a9f742700fe5
keywords:
- Attributo object MIDL
topic_type:
- apiref
api_name:
- object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ddf51e020cdcd5d13dde6938a58ea5e51f22d9dd03f8632312b3d6b8453a9ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118383509"
---
# <a name="object-attribute"></a>object (attributo)

**\[ L'attributo \] dell'interfaccia** dell'oggetto identifica un'interfaccia COM. Un elenco di attributi di interfaccia che non include **\[ l'attributo \] dell'oggetto** indica un'interfaccia RPC DCE.

``` syntax
[ 
    object, 
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

*string-uuid* 
</dt> <dd>

Stringa UUID generata dall'utilità Uuidgen. È possibile racchiudere la stringa UUID tra virgolette.

</dd> <dt>

*interface-attribute-list* 
</dt> <dd>

Altri attributi che si applicano all'interfaccia nel suo complesso.

</dd> <dt>

*interface-name* 
</dt> <dd>

Nome dell'interfaccia.

</dd> <dt>

*interfaccia di base* 
</dt> <dd>

Interfaccia COM da cui deriva questa interfaccia. L'interfaccia di base deve essere [**IUnknown,**](/windows/win32/api/unknwn/nn-unknwn-iunknown) [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)o un'altra interfaccia COM che deriva, direttamente o indirettamente, da **IUnknown** o **IDispatch.**

</dd> </dl>

## <a name="remarks"></a>Commenti

Un elenco di attributi di interfaccia per un'interfaccia COM deve includere **\[** [**l'attributo uuid,**](uuid.md) **\]** ma non può includere l'attributo **\[** [**version.**](version.md) **\]**

Per impostazione predefinita, la compilazione di un'interfaccia COM con il compilatore MIDL genera i file necessari per compilare una DLL proxy. Questa DLL contiene il codice per supportare l'utilizzo dell'interfaccia COM personalizzata da parte di applicazioni client e server oggetti. Tuttavia, se l'elenco di attributi di interfaccia per un'interfaccia COM specifica l'attributo locale, il **\[** [](local.md) **\]** compilatore MIDL genera solo il file di intestazione dell'interfaccia.

Il compilatore MIDL genera automaticamente un tipo di dati di interfaccia per un'interfaccia COM. In alternativa, è possibile usare [**typedef**](typedef.md) con la parola chiave [**interface**](interface.md) per definire in modo esplicito un tipo di dati di interfaccia. La specifica dell'interfaccia può quindi usare il tipo di dati interface nei parametri di funzione e nei valori restituiti, [**nei membri di struct**](struct.md) e [**unione**](union.md) e in altre dichiarazioni di tipo. L'esempio seguente illustra l'uso di un tipo di dati [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) generato automaticamente:

``` syntax
[
    object, 
    uuid (ABCDEFOO-1234-1234-5678-ABCDEF123456)
] 
interface IStream : IUnknown
{ 
    typedef IStream * LPSTREAM; 
    // Other interface definition statements.
}
```

In un'interfaccia COM si presuppone che tutte le funzioni membro dell'interfaccia siano funzioni virtuali. Una funzione virtuale ha un **puntatore this** implicito come primo parametro. La tabella delle funzioni virtuali contiene una voce per ogni funzione membro di interfaccia.

Le funzioni **\[** [**membro**](local.md) **\]** dell'interfaccia oggetto non locale devono avere un valore restituito HRESULT o SCODE. Si noti che le versioni precedenti di MIDL consentiva alle funzioni membro di restituire [**void**](void.md). Tuttavia, a partire da MIDL versione 3.0, la restituzione di **void** genera un errore del compilatore. Se il valore restituito è HRESULT o SCODE, se viene generata un'eccezione durante una chiamata remota, i proxy generati rilevano l'eccezione e restituiscono il codice dell'eccezione nel valore restituito. Se l'applicazione può permettersi di ignorare gli errori che si verificano durante una chiamata di procedura remota, è possibile specificare HRESULT come tipo restituito senza controllare il valore restituito dopo la chiamata.

Se si ricompila un'applicazione precedente, la modifica dei tipi restituiti può causare problemi di compatibilità con le versioni precedenti quando il server invia il risultato appena introdotto al client. In alternativa alla modifica del tipo restituito, è possibile etichettare la funzione che restituisce [**void**](void.md) con la chiamata **\[** [**\_**](call-as.md) **\]** come attributo, rendendola quindi una funzione locale. Definire quindi una funzione remota correlata con gli stessi parametri ma con il tipo restituito di HRESULT. La funzione locale può generare un'eccezione in base a tale valore HRESULT, se necessario.

**\[ L'attributo \]** object non è disponibile quando si esegue la compilazione usando l'opzione [**/osf del compilatore**](-osf.md) MIDL.

## <a name="examples"></a>Esempi

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC), 
    object
] 
interface IMyInterface : IUnknown
{
    // Interface definition statements.
}

[
    uuid(87654321-1234-1234-1234-123456789ABC), 
    object, 
    local
] 
interface ILocalInterface : ISomeOldCOMInterface
{
    // Interface definition statements.
}
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[**call \_ as**](call-as.md)
</dt> <dt>

[File di definizione dell'interfaccia (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**iid \_ is**](iid-is.md)
</dt> <dt>

[**Interfaccia**](interface.md)
</dt> <dt>

[**Locale**](local.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[**Typedef**](typedef.md)
</dt> <dt>

[**Uuid**](uuid.md)
</dt> <dt>

[**Versione**](version.md)
</dt> </dl>

 

 