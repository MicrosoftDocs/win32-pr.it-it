---
title: object (attributo)
description: L'attributo \ Object \ Interface identifica un'interfaccia COM.
ms.assetid: 51e34ef3-eea7-45f4-b961-a9f742700fe5
keywords:
- attributo oggetto MIDL
topic_type:
- apiref
api_name:
- object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb2c21246282646dcf6ae488411316e07ab62b2f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103726335"
---
# <a name="object-attribute"></a>object (attributo)

L'attributo dell'interfaccia dell' **\[ oggetto \]** identifica un'interfaccia com. Un elenco di attributi di interfaccia che non include l'attributo **\[ Object \]** indica un'interfaccia RPC DCE.

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

*stringa-UUID* 
</dt> <dd>

Stringa UUID generata dall'utilità uuidgen. È possibile racchiudere la stringa UUID tra virgolette.

</dd> <dt>

*Interface-Attribute-List* 
</dt> <dd>

Altri attributi applicabili all'interfaccia nel suo complesso.

</dd> <dt>

*Nome interfaccia* 
</dt> <dd>

Nome dell'interfaccia.

</dd> <dt>

*interfaccia di base* 
</dt> <dd>

Interfaccia COM da cui deriva questa interfaccia. L'interfaccia di base deve essere [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)o un'altra interfaccia com che deriva direttamente o indirettamente da **IUnknown** o da **IDispatch**.

</dd> </dl>

## <a name="remarks"></a>Commenti

Un elenco di attributi di interfaccia per un'interfaccia COM deve includere l' **\[** attributo [**UUID**](uuid.md) **\]** , ma non può includere l' **\[** [](version.md) **\]** attributo Version.

Per impostazione predefinita, la compilazione di un'interfaccia COM con il compilatore MIDL genera i file necessari per compilare una DLL proxy. Questa DLL contiene il codice per supportare l'utilizzo dell'interfaccia COM personalizzata da parte delle applicazioni client e dei server oggetti. Tuttavia, se l'elenco di attributi di interfaccia per un'interfaccia COM specifica l' **\[** [](local.md) **\]** attributo locale, il compilatore MIDL genera solo il file di intestazione dell'interfaccia.

Il compilatore MIDL genera automaticamente un tipo di dati dell'interfaccia per un'interfaccia COM. In alternativa, è possibile utilizzare [**typedef**](typedef.md) con la parola chiave [**Interface**](interface.md) per definire in modo esplicito un tipo di dati dell'interfaccia. La specifica dell'interfaccia può quindi utilizzare il tipo di dati dell'interfaccia nei parametri della funzione e i valori restituiti, i membri [**struct**](struct.md) e [**Union**](union.md) e altre dichiarazioni di tipo. Nell'esempio seguente viene illustrato l'utilizzo di un tipo di dati [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) generato automaticamente:

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

In un'interfaccia COM, si presuppone che tutte le funzioni membro di interfaccia siano funzioni virtuali. Una funzione virtuale ha un puntatore **this** implicito come primo parametro. La tabella della funzione virtuale contiene una voce per ogni funzione membro di interfaccia.

**\[**[](local.md) **\]** Le funzioni membro di interfaccia a oggetti non locali devono avere un valore restituito HRESULT o SCODE. Si noti che le versioni precedenti di MIDL hanno consentito alle funzioni membro di restituire [**void**](void.md). Tuttavia, a partire da MIDL versione 3,0, restituendo **void** genera un errore del compilatore. Se si dispone di un valore restituito HRESULT o SCODE significa che se viene generata un'eccezione durante una chiamata remota, i proxy generati intercettano l'eccezione e restituiscono il codice di eccezione nel valore restituito. Se l'applicazione può permettersi di ignorare gli errori che si verificano durante una chiamata di procedura remota, è possibile specificare HRESULT come tipo restituito senza controllare il valore restituito dopo la chiamata.

Se si sta ricompilando un'applicazione precedente, la modifica dei tipi restituiti può presentare problemi di compatibilità con le versioni precedenti quando il server invia il risultato appena introdotto al client. In alternativa alla modifica del tipo restituito, è possibile etichettare la funzione che restituisce [**void**](void.md) con la **\[** [**chiamata \_ come**](call-as.md) **\]** attributo, rendendola così una funzione locale. Definire quindi una funzione remota correlata con gli stessi parametri, ma con il tipo restituito HRESULT. La funzione locale può generare un'eccezione in base al valore HRESULT, se necessario.

L'attributo **\[ \] Object** non è disponibile quando si esegue la compilazione con l'opzione [**/OSF**](-osf.md) del compilatore MIDL.

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

[**chiama \_ come**](call-as.md)
</dt> <dt>

[File di definizione dell'interfaccia (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**IID \_ è**](iid-is.md)
</dt> <dt>

[**interfaccia**](interface.md)
</dt> <dt>

[**locale**](local.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[**typedef**](typedef.md)
</dt> <dt>

[**uuid**](uuid.md)
</dt> <dt>

[**Versione**](version.md)
</dt> </dl>

 

 