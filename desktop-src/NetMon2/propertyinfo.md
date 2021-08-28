---
description: La struttura dei dati PROPERTYINFO definisce una proprietà del protocollo.
ms.assetid: 878777ab-141d-4cc5-b0c1-f2ac8f770bf0
title: Struttura PROPERTYINFO (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PROPERTYINFO
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 8dc20b94fbf889b4c04712eadbee5d7d834d3cf260962fe01ef7837e5893c4a4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120128951"
---
# <a name="propertyinfo-structure"></a>Struttura PROPERTYINFO

La struttura dei dati **PROPERTYINFO** definisce una proprietà del protocollo.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _PROPERTYINFO {
  HPROPERTY hProperty;
  DWORD     Version;
  LPSTR     Label;
  LPSTR     Comment;
  BYTE      DataType;
  BYTE      DataQualifier;
  union {
    LPVOID  lpExtendedInfo;
    LPRANGE lpRange;
    LPSET   lpSet;
    DWORD   Bitmask;
    DWORD   Value;
  };
  WORD      FormatStringSize;
  LPVOID    InstanceData;
} PROPERTYINFO, *LPPROPERTYINFO;
```



## <a name="members"></a>Members

<dl> <dt>

**hProperty**
</dt> <dd>

Impostare questo campo su zero. Nell'output, Network Monitor restituisce un handle alla proprietà dopo l'aggiunta della proprietà al database delle proprietà.

</dd> <dt>

**Version**
</dt> <dd>

Riservato. Deve essere impostato su zero.

</dd> <dt>

**Etichetta**
</dt> <dd>

Nome della proprietà.

</dd> <dt>

**Commento**
</dt> <dd>

Descrizione della proprietà. La descrizione viene visualizzata nella Network Monitor di stato.

</dd> <dt>

**DataType**
</dt> <dd>

Tipo di dati della proprietà. Questo membro può avere uno dei valori seguenti.



| Valore                                                                                                                                                                                                       | Significato                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PROP_TYPE_VOID"></span><span id="prop_type_void"></span><dl> <dt>**PROP \_ TYPE \_ VOID**</dt> </dl>                                           | Tipo di proprietà sconosciuto. Non esiste una lunghezza o un formato implicito.<br/>                                                                                                                                                                                                                                  |
| <span id="PROP_TYPE_SUMMARY"></span><span id="prop_type_summary"></span><dl> <dt>**RIEPILOGO \_ DEL TIPO DI \_ PROPRIETÀ**</dt> </dl>                                  | Riepilogo del tipo di proprietà. Indica la prima istanza della proprietà collegata dal parser a un frame. PROP \_ TYPE SUMMARY può essere utilizzato come \_ segnaposto per i gruppi di proprietà. Questo valore indica che la proprietà non è definita nel protocollo *RFC*.<br/> |
| <span id="PROP_TYPE_BYTE"></span><span id="prop_type_byte"></span><dl> <dt>**PROP \_ TYPE \_ BYTE**</dt> </dl>                                           | Dati numerici con dimensioni di un byte (entità a 8 bit).<br/>                                                                                                                                                                                                                                             |
| <span id="PROP_TYPE_WORD"></span><span id="prop_type_word"></span><dl> <dt>**PROP \_ TYPE \_ WORD**</dt> </dl>                                           | Dati numerici con dimensioni di due byte (entità a 16 bit).<br/>                                                                                                                                                                                                                                           |
| <span id="PROP_TYPE_DWORD"></span><span id="prop_type_dword"></span><dl> <dt>**PROP \_ TYPE \_ DWORD**</dt> </dl>                                        | Dati numerici con dimensioni di quattro byte (entità a 32 bit).<br/>                                                                                                                                                                                                                                          |
| <span id="PROP_TYPE_LARGEINT"></span><span id="prop_type_largeint"></span><dl> <dt>**TIPO PROP \_ \_ LARGEINT**</dt> </dl>                               | Dati numerici con dimensioni di otto byte (entità a 64 bit).<br/>                                                                                                                                                                                                                                         |
| <span id="PROP_TYPE_ADDR"></span><span id="prop_type_addr"></span><dl> <dt>**PROP \_ TYPE \_ ADDR**</dt> </dl>                                           | Indirizzo MAC (entità a 6 byte).<br/>                                                                                                                                                                                                                                                                     |
| <span id="PROP_TYPE_TIME"></span><span id="prop_type_time"></span><dl> <dt>**PROP \_ TYPE \_ TIME**</dt> </dl>                                           | **Struttura SYSTEMTIME.**<br/>                                                                                                                                                                                                                                                                        |
| <span id="PROP_TYPE_STRING"></span><span id="prop_type_string"></span><dl> <dt>**PROP \_ TYPE \_ STRING**</dt> </dl>                                     | Dati di testo ASCII. Questo tipo di dati non termina con NULL. <br/> Per i dati Unicode, quando si specificano dati di testo ASCII, è necessario impostare anche il flag UNICODE IFLAG quando viene chiamata la funzione di istanza \_ della proprietà di collegamento.<br/>                                                                          |
| <span id="PROP_TYPE_IP_ADDRESS"></span><span id="prop_type_ip_address"></span><dl> <dt>**INDIRIZZO \_ IP DI TIPO \_ \_ PROP**</dt> </dl>                        | Indirizzo IP. (entità a 4 byte).<br/>                                                                                                                                                                                                                                                                     |
| <span id="PROP_TYPE_IPX_ADDRESS"></span><span id="prop_type_ipx_address"></span><dl> <dt>**PROP \_ TYPE \_ IPX \_ ADDRESS**</dt> </dl>                     | Indirizzo IPX. (entità a 10 byte).<br/>                                                                                                                                                                                                                                                                   |
| <span id="PROP_TYPE_BYTESWAPPED_WORD"></span><span id="prop_type_byteswapped_word"></span><dl> <dt>**PROP \_ TYPE \_ BYTESWAPPED \_ WORD**</dt> </dl>      | Obsoleta. Per i dati WORD scambiati in byte, impostare **DataType** su PROP TYPE WORD e impostare il \_ flag IFLAG SWAPPED quando si chiama una funzione di istanza \_ della proprietà \_ **Attach.**<br/>                                                                                                                                |
| <span id="PROP_TYPE_BYTESWAPPED_DWORD"></span><span id="prop_type_byteswapped_dword"></span><dl> <dt>**PROP \_ TYPE \_ BYTESWAPPED \_ DWORD**</dt> </dl>   | Obsoleta. Per i dati DWORD scambiati in byte, impostare **DataType** su PROP TYPE DWORD e impostare il \_ flag IFLAG SWAPPED quando si chiama una funzione di istanza \_ della proprietà \_ **Attach.**<br/>                                                                                                                              |
| <span id="PROP_TYPE_TYPED_STRING"></span><span id="prop_type_typed_string"></span><dl> <dt>**STRINGA \_ \_ TIPIZZATO DI \_ PROP**</dt> </dl>                  | Obsoleta. Per i dati stringa di tipo variabile, impostare **DataType** su PROP TYPE STRING e impostare il flag UNICODE IFLAG quando si chiama una funzione di istanza \_ della proprietà \_ \_ Attach. <br/>                                                                                                                           |
| <span id="PROP_TYPE_RAW_DATA"></span><span id="prop_type_raw_data"></span><dl> <dt>**DATI NON \_ ELABORATI \_ DI TIPO \_ PROP**</dt> </dl>                              | Dati non elaborati di lunghezza e formato sconosciuti.<br/>                                                                                                                                                                                                                                                           |
| <span id="PROP_TYPE_COMMENT"></span><span id="prop_type_comment"></span><dl> <dt>**PROP \_ TYPE \_ COMMENT**</dt> </dl>                                  | Uguale a PROP \_ TYPE \_ VOID.<br/>                                                                                                                                                                                                                                                                        |
| <span id="PROP_TYPE_SRCFRIENDLYNAME"></span><span id="prop_type_srcfriendlyname"></span><dl> <dt>**PROP \_ TYPE \_ SRCFRIENDLYNAME**</dt> </dl>          | Indirizzo del nome descrittivo dell'origine. Network Monitor non fornisce il supporto della formattazione predefinito per questo tipo di dati.<br/>                                                                                                                                                                                |
| <span id="PROP_TYPE_DSTFRIENDLYNAME"></span><span id="prop_type_dstfriendlyname"></span><dl> <dt>**PROP \_ TYPE \_ DSTFRIENDLYNAME**</dt> </dl>          | Indirizzo del nome descrittivo della destinazione. Network Monitor non fornisce il supporto della formattazione predefinito per questo tipo di dati.<br/>                                                                                                                                                                           |
| <span id="PROP_TYPE_TOKENRING_ADDRESS"></span><span id="prop_type_tokenring_address"></span><dl> <dt>**PROP \_ TYPE \_ TOKENRING \_ ADDRESS**</dt> </dl>   | Indirizzo token ring. Network Monitor non fornisce il supporto della formattazione predefinito per questo tipo di dati.<br/>                                                                                                                                                                                             |
| <span id="PROP_TYPE_FDDI_ADDRESS"></span><span id="prop_type_fddi_address"></span><dl> <dt>**PROP \_ TYPE \_ FDDI \_ ADDRESS**</dt> </dl>                  | Indirizzo FDDI. Network Monitor non fornisce il supporto della formattazione predefinito per questo tipo di dati.<br/>                                                                                                                                                                                                   |
| <span id="PROP_TYPE_ETHERNET_ADDRESS"></span><span id="prop_type_ethernet_address"></span><dl> <dt>**PROP \_ TYPE \_ ETHERNET \_ ADDRESS**</dt> </dl>      | Indirizzo Ethernet. Network Monitor non fornisce il supporto della formattazione predefinito per questo tipo di dati.<br/>                                                                                                                                                                                               |
| <span id="PROP_TYPE_OBJECT_IDENTIFIER"></span><span id="prop_type_object_identifier"></span><dl> <dt>**IDENTIFICATORE \_ \_ DELL'OGGETTO DI TIPO \_ PROP**</dt> </dl>   | Identificatore di oggetto SNMP con codifica BER.<br/>                                                                                                                                                                                                                                                              |
| <span id="PROP_TYPE_VINES_IP_ADDRESS"></span><span id="prop_type_vines_ip_address"></span><dl> <dt>**PROP \_ TYPE \_ VINES \_ IP \_ ADDRESS**</dt> </dl>     | Indirizzo IP vines (entità a 6 byte).<br/>                                                                                                                                                                                                                                                                |
| <span id="PROP_TYPE_VAR_LEN_SMALL_INT"></span><span id="prop_type_var_len_small_int"></span><dl> <dt>**PROP \_ TYPE \_ VAR \_ LEN \_ SMALL \_ INT**</dt> </dl> | Valore numerico senza lunghezza predeterminato, ma con lunghezza non superiore a 8 byte. La lunghezza dei dati collegati determina la lunghezza del valore.<br/>                                                                                                                                                |



 

</dd> <dt>

**DataQualifier**
</dt> <dd>

Qualificatore di dati di una proprietà. Questo membro fornisce informazioni precise sul tipo di dati.

**DataQualifier** può avere uno dei valori seguenti.



| Valore                                                                                                                                                                                                  | Significato                                                                                                                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PROP_QUAL_NONE"></span><span id="prop_qual_none"></span><dl> <dt>**PROP \_ QUAL \_ NONE**</dt> </dl>                                      | Il tipo di dati della proprietà è l'unica specifica della proprietà. <br/> Quando questo valore è impostato, il membro unione della struttura viene impostato su **NULL** e quindi ignorato.<br/>                                                                                                                                        |
| <span id="PROP_QUAL_RANGE"></span><span id="prop_qual_range"></span><dl> <dt>**PROP \_ QUAL \_ RANGE**</dt> </dl>                                   | Si prevede che il valore numerico sia compreso in un intervallo specificato. Definire l'intervallo nel **membro lpRange.**<br/>                                                                                                                                                                                                                |
| <span id="PROP_QUAL_SET"></span><span id="prop_qual_set"></span><dl> <dt>**PROP \_ QUAL \_ SET**</dt> </dl>                                         | Il valore di una proprietà viene confrontato con un set di valori specificati nel membro **lpSet** dell'unione della struttura. Il valore di una proprietà può essere **BYTE,** **WORD,** **DWORD,** **LARGEINT** o **TIME.**<br/>                                                                                                |
| <span id="PROP_QUAL_BITFIELD"></span><span id="prop_qual_bitfield"></span><dl> <dt>**PROP \_ QUAL \_ BITFIELD**</dt> </dl>                          | Obsoleta.<br/>                                                                                                                                                                                                                                                                                                            |
| <span id="PROP_QUAL_LABELED_SET"></span><span id="prop_qual_labeled_set"></span><dl> <dt>**SET CON ETICHETTA PROP \_ QUAL \_ \_**</dt> </dl>                | Il valore di una proprietà viene confrontato con un valore in un set di coppie di etichette di valori. Le coppie di etichette valore vengono specificate nel **membro lpSet** dell'unione della struttura. <br/> In fase di visualizzazione, se il valore della proprietà corrisponde a un valore nel set, vengono visualizzati sia un valore che l'etichetta associata.<br/> |
| <span id="PROP_QUAL_LABELED_BITFIELD"></span><span id="prop_qual_labeled_bitfield"></span><dl> <dt>**PROP \_ QUAL CON ETICHETTA \_ \_ BITFIELD**</dt> </dl> | Obsoleta. In alternativa, usare PROP \_ QUAL \_ FLAGS.<br/>                                                                                                                                                                                                                                                                             |
| <span id="PROP_QUAL_CONST"></span><span id="prop_qual_const"></span><dl> <dt>**PROP \_ QUAL \_ CONST**</dt> </dl>                                   | Il valore di una proprietà viene confrontato con una costante specificata nel membro **Value** dell'unione. <br/> In fase di visualizzazione, se i valori della proprietà e la costante non corrispondono, viene visualizzato un messaggio di errore formattato con il valore impostato su Normale.<br/>                                                             |
| <span id="PROP_QUAL_FLAGS"></span><span id="prop_qual_flags"></span><dl> <dt>**FLAG PROP \_ QUAL \_**</dt> </dl>                                   | Il valore della proprietà viene confrontato con i BIT specifici identificati nel membro **lpSet** dell'unione.<br/>                                                                                                                                                                                                              |
| <span id="PROP_QUAL_ARRAY"></span><span id="prop_qual_array"></span><dl> <dt>**PROP \_ QUAL \_ ARRAY**</dt> </dl>                                   | Il valore di una proprietà specifica una matrice di valori. La lunghezza dei dati associati determina la lunghezza di una matrice. <br/> Quando il valore PROP QUAL ARRAY è impostato, il membro di unione della struttura di dati \_ \_ **PROPERTYINFO** viene impostato su **NULL** e ignorato.<br/>                                                    |



 

</dd> <dt>

**lpExtendedInfo**
</dt> <dd>

Riservato (membro dell'unione).

</dd> <dt>

**lpRange**
</dt> <dd>

Puntatore a [una struttura RANGE](range.md) che definisce un intervallo di valori. Questo membro deve essere impostato se **il membro DataQualifier** di questa struttura è impostato su PROP \_ QUAL RANGE \_ (membro dell'unione).

</dd> <dt>

**lpSet**
</dt> <dd>

Puntatore a [una struttura SET](set.md) che specifica un set di valori o etichette. Questo membro deve essere impostato se il **membro DataQualifier** della struttura è impostato su PROP \_ QUAL SET, PROP QUAL LABELED SET o PROP QUAL FLAGS \_ \_ \_ \_ \_ \_ (membro dell'unione).

</dd> <dt>

**Maschera**
</dt> <dd>

Obsoleto (membro dell'unione).

</dd> <dt>

**Valore**
</dt> <dd>

Valore costante utilizzato quando **DataQualifier** è impostato su PROP \_ QUAL \_ CONST (membro dell'unione).

</dd> <dt>

**FormatStringSize**
</dt> <dd>

Dimensioni massime usate solo per la descrizione della proprietà.

</dd> <dt>

**Instancedata**
</dt> <dd>

Specificare la funzione di formato chiamata per formattare i dati visualizzati per la proprietà . Per usare il formattatore generico, specificare la **funzione FormatPropertyInstance.**

</dd> </dl>

## <a name="remarks"></a>Commenti

La **struttura PROPERTYINFO** viene usata nelle chiamate alla [funzione AddProperty.](/previous-versions/bb251873(v=msdn.10)) La **funzione AddProperty** aggiunge una singola definizione di proprietà al database delle [*proprietà del parser.*](p.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[AddProperty](/previous-versions/bb251873(v=msdn.10))
</dt> <dt>

[Gamma](range.md)
</dt> <dt>

[SET](set.md)
</dt> </dl>

 

