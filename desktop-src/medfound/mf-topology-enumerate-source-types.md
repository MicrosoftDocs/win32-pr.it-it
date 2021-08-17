---
description: Specifica se il caricatore della topologia enumera i tipi di supporti forniti dall'origine multimediale.
ms.assetid: 2675ef16-2018-47e8-bb22-2fc0d62e6681
title: MF_TOPOLOGY_ENUMERATE_SOURCE_TYPES attributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cc9ff7cf9e1497f0d15f68e68c254483f0c9f074e2ce4204e9d77d84aee4ea8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117691297"
---
# <a name="mf_topology_enumerate_source_types-attribute"></a>Attributo MF \_ TOPOLOGY \_ ENUMERATE SOURCE \_ \_ TYPES

Specifica se il caricatore della topologia enumera i tipi di supporti forniti dall'origine multimediale.

## <a name="data-type"></a>Tipo di dati

**UINT32**

Usare uno dei valori seguenti.



| Valore                                                                                                                                    | Significato                                             |
|------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="FALSE"></span><span id="false"></span><dl> <dt>FALSE****</dt> </dl> | Non enumerare i tipi di supporti di origine.<br/> |
| <span id="TRUE"></span><span id="true"></span><dl> <dt>TRUE****</dt> </dl>    | Enumerare i tipi di supporti di origine.<br/>        |



 

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Per impostare questo attributo, chiamare [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Si applica a

[**Topologia IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a>Commenti

Ogni flusso in un'origine multimediale può offrire più di un tipo di supporto. L'elenco di tipi viene enumerato tramite [**l'interfaccia IMFMediaTypeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) nel descrittore di flusso.

L'ordine in cui il caricatore della topologia prova i tipi di supporti di un'origine multimediale è controllato da due attributi:

-   Attributo MF \_ TOPOLOGY \_ ENUMERATE SOURCE TYPES \_ nella \_ topologia.
-   Attributo [**MF \_ TOPONODE \_ CONNECT \_ METHOD**](mf-toponode-connect-method-attribute.md) nel nodo di origine.

Se l'attributo MF TOPOLOGY ENUMERATE SOURCE TYPES è FALSE o non è impostato, il caricatore della topologia usa il tipo di supporto \_ \_ corrente del \_ \_ flusso.  Non enumera l'elenco dei tipi possibili. Se il tipo di supporto corrente non è compatibile con il nodo della topologia downstream e non è possibile trovare alcuna combinazione di decodificatori/convertitori, la risoluzione della topologia ha esito negativo.

Se l'attributo MF TOPOLOGY ENUMERATE SOURCE TYPES è TRUE, il caricatore della topologia enumera i tipi di supporti dell'origine finché non trova \_ \_ un tipo \_ \_ compatibile.  In tal caso, l'ordine esatto delle operazioni dipende dal fatto che l'attributo [**MF \_ TOPONODE \_ CONNECT \_ METHOD**](mf-toponode-connect-method-attribute.md) nel nodo di origine includa il flag **MF \_ CONNECT RESOLVE \_ \_ INDEPENDENT \_ OUTPUTTYPES.**

Se MF TOPOLOGY ENUMERATE SOURCE TYPES è TRUE e il \_ \_ flag \_ \_ **MF \_ CONNECT RESOLVE INDEPENDENT \_ \_ \_ OUTPUTTYPES** è impostato,  il caricatore della topologia esaurirà ogni tipo di supporto prima di passare al successivo, come indicato di seguito:

``` syntax
foreach media type T
    connect directly using T
    if failed, connect with converters using T
    if failed, connect with decoders using T
```

Se MF TOPOLOGY ENUMERATE SOURCE TYPES è TRUE ma \_ \_ \_ MF CONNECT RESOLVE \_ **INDEPENDENT \_ \_ \_ \_ OUTPUTTYPES**  non è impostato, il caricatore della topologia tenta una connessione diretta con ogni tipo di supporto, quindi prova ogni tipo di supporto con convertitori e infine prova ogni tipo di supporto con decodificatori:

``` syntax
foreach media type T
    connect directly using T
if failed,
    foreach media type T
        connect with converters using T
if failed
    foreach media type T
        connect with decoders using T
```

Se MF \_ TOPOLOGY \_ ENUMERATE SOURCE TYPES è \_ \_ **FALSE,** il flag **MF CONNECT RESOLVE INDEPENDENT \_ \_ \_ \_ OUTPUTTYPES** viene ignorato.

Il valore predefinito di MF \_ TOPOLOGY \_ ENUMERATE SOURCE TYPES è FALSE per garantire la \_ \_ compatibilità con le applicazioni esistenti. 

La costante GUID per questo attributo viene esportata da mfuuid.lib.

### <a name="example"></a>Esempio

Di seguito è riportato un esempio che illustra il flag **MF \_ CONNECT RESOLVE \_ INDEPENDENT \_ \_ OUTPUTTYPES.** Si supponga che per la topologia l'attributo \_ MF TOPOLOGY \_ ENUMERATE SOURCE TYPES sia impostato su \_ \_ **TRUE.**

L'origine multimediale offre i tipi seguenti:

-   T1, T2, T3

Il sink multimediale accetta i tipi seguenti:

-   T3, T4

Caso 1: il flag **MF \_ CONNECT RESOLVE \_ INDEPENDENT \_ \_ OUTPUTTYPES** è impostato.

1.  Il caricatore della topologia tenta una connessione diretta con T1. Il sink rifiuta T1.
2.  Il caricatore della topologia inserisce un decodificatore che accetta T1 e restituisce T4. Il sink accetta T4.
3.  La topologia finale contiene: origine dei supporti → decodificatore → sink multimediale.

Caso 2: il flag non è impostato.

1.  Il caricatore della topologia tenta una connessione diretta con T1. Il sink rifiuta T1.
2.  Il caricatore della topologia tenta una connessione diretta con T2. Il sink rifiuta T2.
3.  Il caricatore della topologia tenta una connessione diretta con T3. Il sink accetta T3.
4.  La topologia finale contiene: origine dei supporti → sink multimediale.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                         |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/>                            |
| Intestazione<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico di Media Foundation attributi](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributi della topologia](topology-attributes.md)
</dt> </dl>

 

 




