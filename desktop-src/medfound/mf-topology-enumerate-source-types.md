---
description: Specifica se il caricatore della topologia enumera i tipi di supporto forniti dall'origine multimediale.
ms.assetid: 2675ef16-2018-47e8-bb22-2fc0d62e6681
title: Attributo MF_TOPOLOGY_ENUMERATE_SOURCE_TYPES (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 015042bbf9994f81058c621239224196e6ec9ac8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343311"
---
# <a name="mf_topology_enumerate_source_types-attribute"></a>\_Attributo della topologia MF \_ enumerazione di \_ tipi di origine \_

Specifica se il caricatore della topologia enumera i tipi di supporto forniti dall'origine multimediale.

## <a name="data-type"></a>Tipo di dati

**UINT32**

Usare uno dei valori seguenti.



| Valore                                                                                                                                    | Significato                                             |
|------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="FALSE"></span><span id="false"></span><dl> <dt>FALSE * * * *</dt> </dl> | Non enumerare i tipi di supporto di origine.<br/> |
| <span id="TRUE"></span><span id="true"></span><dl> <dt>TRUE * * * *</dt> </dl>    | Enumerare i tipi di supporto di origine.<br/>        |



 

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)SetAttribute.

## <a name="applies-to"></a>Si applica a

[**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a>Commenti

Ogni flusso in un'origine multimediale può offrire più di un tipo di supporto. L'elenco dei tipi viene enumerato tramite l'interfaccia [**IMFMediaTypeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) sul descrittore del flusso.

L'ordine in cui il caricatore della topologia Cerca i tipi di supporto di un'origine multimediale è controllato da due attributi:

-   L' \_ attributo della topologia MF \_ enumera \_ \_ i tipi di origine nella topologia.
-   Attributo [**del \_ \_ \_ Metodo MF TOPONODE Connect**](mf-toponode-connect-method-attribute.md) nel nodo di origine.

Se l' \_ attributo della topologia MF \_ enumerazione dei \_ \_ tipi di origine è **false** o non impostato, il caricatore della topologia usa il tipo di supporto corrente del flusso. Non enumera l'elenco dei tipi possibili. Se il tipo di supporto corrente non è compatibile con il nodo della topologia downstream e non è possibile trovare una combinazione di decodificatori/convertitori, la risoluzione della topologia ha esito negativo.

Se l' \_ attributo della topologia MF \_ enumerazione dei tipi di \_ origine \_ è **true**, il caricatore della topologia enumera i tipi di supporto dell'origine finché non trova un tipo compatibile. In tal caso, l'ordine esatto delle operazioni varia a seconda che l'attributo [**del \_ \_ \_ Metodo MF TOPONODE Connect**](mf-toponode-connect-method-attribute.md) nel nodo di origine includa il flag OutputType per la **\_ \_ risoluzione \_ \_ MF Connect** .

Se la \_ topologia MF \_ enumera \_ \_ i tipi di origine è **true** e si imposta il flag **MF \_ Connect \_ Resolve \_ Independent \_ OutputType** , il caricatore della topologia esaurisce ogni tipo di supporto prima di procedere al passaggio successivo, come indicato di seguito:

``` syntax
foreach media type T
    connect directly using T
    if failed, connect with converters using T
    if failed, connect with decoders using T
```

Se \_ la topologia MF \_ enumera i \_ \_ tipi di origine è **true** , ma non è impostata la **\_ soluzione MF Connect \_ Resolve \_ Independent \_ OutputType** , il caricatore della topologia tenta una connessione diretta a ogni tipo di supporto, quindi tenta ogni tipo di supporto con i convertitori e infine Cerca ogni tipo di supporto con i decodificatori:

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

Se \_ la topologia MF per l' \_ enumerazione \_ \_ dei tipi di origine è **false**, il flag OutputType per la **\_ \_ risoluzione \_ \_ MF Connect** viene ignorato.

Il valore predefinito della \_ topologia MF \_ enumerazione dei tipi di \_ origine \_ è **false** per compatibilità con le applicazioni esistenti.

La costante GUID per questo attributo viene esportata da mfuuid. lib.

### <a name="example"></a>Esempio

Di seguito è riportato un esempio in cui viene illustrato il flag **MF \_ Connect \_ Resolve \_ Independent \_ OutputType** . Si supponga che la topologia includa l' \_ attributo della topologia MF \_ enumerazione dei \_ \_ tipi di origine impostato su **true**.

L'origine multimediale offre i tipi seguenti:

-   T1, T2, T3

Il sink multimediale accetta i tipi seguenti:

-   T3, T4

Caso 1: è impostato il flag per la **\_ risoluzione dei \_ \_ \_ OutputType indipendenti MF Connect** .

1.  Il caricatore della topologia tenta una connessione diretta con T1. Il sink rifiuta T1.
2.  Il caricatore della topologia inserisce un decodificatore che accetta T1 e output T4. Il sink accetta T4.
3.  La topologia finale contiene: origine multimediale → decodificatore → sink multimediale.

Caso 2: il flag non è impostato.

1.  Il caricatore della topologia tenta una connessione diretta con T1. Il sink rifiuta T1.
2.  Il caricatore della topologia tenta una connessione diretta con T2. Il sink rifiuta T2.
3.  Il caricatore della topologia tenta una connessione diretta con T3. Il sink accetta T3.
4.  La topologia finale contiene: origine multimediale → sink multimediale.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                         |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/>                            |
| Intestazione<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributi della topologia](topology-attributes.md)
</dt> </dl>

 

 




