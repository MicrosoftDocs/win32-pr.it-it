---
description: La struttura dei dati PROPERTYINFO definisce una proprietà del protocollo.
ms.assetid: 878777ab-141d-4cc5-b0c1-f2ac8f770bf0
title: Struttura PROPERTYINFO (Netmon. h)
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
ms.openlocfilehash: 435b08c5dd5e020dce2bde9be03a0d41299836c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967240"
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

Impostare questo campo su zero. Nell'output Network Monitor restituisce un handle alla proprietà dopo che la proprietà viene aggiunta al database della proprietà.

</dd> <dt>

**Versione**
</dt> <dd>

Riservato. Deve essere impostato su zero.

</dd> <dt>

**Etichetta**
</dt> <dd>

Nome della proprietà.

</dd> <dt>

**Commento**
</dt> <dd>

Descrizione della proprietà. La descrizione viene visualizzata sulla barra di stato Network Monitor.

</dd> <dt>

**DataType**
</dt> <dd>

Tipo di dati della proprietà. Questo membro può avere uno dei valori seguenti.



| Valore                                                                                                                                                                                                       | Significato                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PROP_TYPE_VOID"></span><span id="prop_type_void"></span><dl> <dt>**\_tipo Prop \_ void**</dt> </dl>                                           | Il tipo di proprietà è sconosciuto. Non esiste alcuna lunghezza o formato implicito.<br/>                                                                                                                                                                                                                                  |
| <span id="PROP_TYPE_SUMMARY"></span><span id="prop_type_summary"></span><dl> <dt>**\_Riepilogo del tipo di Prop \_**</dt> </dl>                                  | Riepilogo del tipo di proprietà. Indica la prima istanza di proprietà che il parser connette a un frame. Il \_ \_ Riepilogo del tipo prop può fungere da segnaposto per gruppi di proprietà. Questo valore indica che la proprietà non è definita nella *RFC* del protocollo.<br/> |
| <span id="PROP_TYPE_BYTE"></span><span id="prop_type_byte"></span><dl> <dt>**tipo di PROP \_ \_ byte**</dt> </dl>                                           | Dati numerici con una dimensione di un byte (entità a 8 bit).<br/>                                                                                                                                                                                                                                             |
| <span id="PROP_TYPE_WORD"></span><span id="prop_type_word"></span><dl> <dt>**tipo di PROP \_ \_ Word**</dt> </dl>                                           | Dati numerici con una dimensione di due byte (entità a 16 bit).<br/>                                                                                                                                                                                                                                           |
| <span id="PROP_TYPE_DWORD"></span><span id="prop_type_dword"></span><dl> <dt>**tipo di PROP \_ \_ DWORD**</dt> </dl>                                        | Dati numerici con una dimensione di quattro byte (entità a 32 bit).<br/>                                                                                                                                                                                                                                          |
| <span id="PROP_TYPE_LARGEINT"></span><span id="prop_type_largeint"></span><dl> <dt>**\_tipo Prop \_ largeInt**</dt> </dl>                               | Dati numerici con una dimensione di otto byte (entità a 64 bit).<br/>                                                                                                                                                                                                                                         |
| <span id="PROP_TYPE_ADDR"></span><span id="prop_type_addr"></span><dl> <dt>**\_tipo Prop \_ addr**</dt> </dl>                                           | Indirizzo MAC (entità a 6 byte).<br/>                                                                                                                                                                                                                                                                     |
| <span id="PROP_TYPE_TIME"></span><span id="prop_type_time"></span><dl> <dt>**\_ora tipo di Prop \_**</dt> </dl>                                           | Struttura **SYSTEMTIME** .<br/>                                                                                                                                                                                                                                                                        |
| <span id="PROP_TYPE_STRING"></span><span id="prop_type_string"></span><dl> <dt>**\_stringa di tipo Prop \_**</dt> </dl>                                     | Dati di testo ASCII. Questo tipo di dati non è con terminazione NULL. <br/> Per i dati Unicode, quando si specificano dati di testo ASCII, è \_ necessario impostare anche il flag Unicode IFLAG quando viene chiamata la funzione di istanza della proprietà di connessione.<br/>                                                                          |
| <span id="PROP_TYPE_IP_ADDRESS"></span><span id="prop_type_ip_address"></span><dl> <dt>**\_ \_ indirizzo IP del tipo Prop \_**</dt> </dl>                        | Indirizzo IP. (entità a 4 byte).<br/>                                                                                                                                                                                                                                                                     |
| <span id="PROP_TYPE_IPX_ADDRESS"></span><span id="prop_type_ipx_address"></span><dl> <dt>**\_ \_ indirizzo IPX di tipo Prop \_**</dt> </dl>                     | Indirizzo IPX. (entità a 10 byte).<br/>                                                                                                                                                                                                                                                                   |
| <span id="PROP_TYPE_BYTESWAPPED_WORD"></span><span id="prop_type_byteswapped_word"></span><dl> <dt>**\_tipo Prop \_ BYTESWAPPED \_ Word**</dt> </dl>      | Obsoleta. Per i dati di WORD con scambio di byte, impostare **DataType** su Prop \_ digitare \_ Word e impostare il \_ flag IFLAG scambiato quando si chiama una funzione di istanza della proprietà di **connessione** .<br/>                                                                                                                                |
| <span id="PROP_TYPE_BYTESWAPPED_DWORD"></span><span id="prop_type_byteswapped_dword"></span><dl> <dt>**\_tipo Prop \_ BYTESWAPPED \_ DWORD**</dt> </dl>   | Obsoleta. Per i dati DWORD con scambio di byte, impostare **DataType** su Prop \_ tipo \_ DWORD e impostare il \_ flag IFLAG scambiato quando si chiama una funzione di istanza della proprietà di **connessione** .<br/>                                                                                                                              |
| <span id="PROP_TYPE_TYPED_STRING"></span><span id="prop_type_typed_string"></span><dl> <dt>**\_ \_ stringa tipizzata di tipo Prop \_**</dt> </dl>                  | Obsoleta. Per i dati di tipo stringa variabile, impostare **DataType** su Prop \_ tipo \_ stringa e impostare il \_ flag Unicode IFLAG quando si chiama una funzione di istanza della proprietà di **connessione** .<br/>                                                                                                                           |
| <span id="PROP_TYPE_RAW_DATA"></span><span id="prop_type_raw_data"></span><dl> <dt>**tipi di PROP \_ \_ dati non elaborati \_**</dt> </dl>                              | Dati non elaborati di lunghezza e formato sconosciuti.<br/>                                                                                                                                                                                                                                                           |
| <span id="PROP_TYPE_COMMENT"></span><span id="prop_type_comment"></span><dl> <dt>**\_commento tipo \_ prop**</dt> </dl>                                  | Uguale al tipo di PROP \_ \_ void.<br/>                                                                                                                                                                                                                                                                        |
| <span id="PROP_TYPE_SRCFRIENDLYNAME"></span><span id="prop_type_srcfriendlyname"></span><dl> <dt>**\_tipo Prop \_ SRCFRIENDLYNAME**</dt> </dl>          | Indirizzo del nome descrittivo dell'origine. Network Monitor non fornisce il supporto predefinito per la formattazione per questo tipo di dati.<br/>                                                                                                                                                                                |
| <span id="PROP_TYPE_DSTFRIENDLYNAME"></span><span id="prop_type_dstfriendlyname"></span><dl> <dt>**\_tipo Prop \_ DSTFRIENDLYNAME**</dt> </dl>          | Indirizzo del nome descrittivo di destinazione. Network Monitor non fornisce il supporto predefinito per la formattazione per questo tipo di dati.<br/>                                                                                                                                                                           |
| <span id="PROP_TYPE_TOKENRING_ADDRESS"></span><span id="prop_type_tokenring_address"></span><dl> <dt>**\_ \_ Indirizzo Tokenring di tipo Prop \_**</dt> </dl>   | Indirizzo token-ring. Network Monitor non fornisce il supporto predefinito per la formattazione per questo tipo di dati.<br/>                                                                                                                                                                                             |
| <span id="PROP_TYPE_FDDI_ADDRESS"></span><span id="prop_type_fddi_address"></span><dl> <dt>**\_ \_ Indirizzo FDDI di tipo Prop \_**</dt> </dl>                  | Indirizzo FDDI. Network Monitor non fornisce il supporto predefinito per la formattazione per questo tipo di dati.<br/>                                                                                                                                                                                                   |
| <span id="PROP_TYPE_ETHERNET_ADDRESS"></span><span id="prop_type_ethernet_address"></span><dl> <dt>**\_ \_ indirizzo Ethernet del tipo Prop \_**</dt> </dl>      | Indirizzo Ethernet. Network Monitor non fornisce il supporto predefinito per la formattazione per questo tipo di dati.<br/>                                                                                                                                                                                               |
| <span id="PROP_TYPE_OBJECT_IDENTIFIER"></span><span id="prop_type_object_identifier"></span><dl> <dt>**\_ \_ identificatore oggetto di tipo Prop \_**</dt> </dl>   | Identificatore di oggetto SNMP con codifica BER.<br/>                                                                                                                                                                                                                                                              |
| <span id="PROP_TYPE_VINES_IP_ADDRESS"></span><span id="prop_type_vines_ip_address"></span><dl> <dt>**\_ \_ indirizzo IP delle viti di tipo \_ prop \_**</dt> </dl>     | Indirizzo IP viti (entità a 6 byte).<br/>                                                                                                                                                                                                                                                                |
| <span id="PROP_TYPE_VAR_LEN_SMALL_INT"></span><span id="prop_type_var_len_small_int"></span><dl> <dt>**\_tipo Prop \_ var \_ Len \_ small \_ int**</dt> </dl> | Valore numerico senza una lunghezza predeterminata, ma non più di 8 byte. La lunghezza dei dati associati determina la lunghezza del valore.<br/>                                                                                                                                                |



 

</dd> <dt>

**Qualificatore dataqualifier**
</dt> <dd>

Qualificatore dei dati di una proprietà. Questo membro fornisce informazioni precise sul tipo di dati.

**Dataqualifier** può avere uno dei valori seguenti.



| Valore                                                                                                                                                                                                  | Significato                                                                                                                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PROP_QUAL_NONE"></span><span id="prop_qual_none"></span><dl> <dt>**PROP \_ qual \_ None**</dt> </dl>                                      | Il tipo di dati della proprietà è l'unica specifica della proprietà. <br/> Quando questo valore è impostato, il membro Union della struttura viene impostato su **null**, quindi viene ignorato.<br/>                                                                                                                                        |
| <span id="PROP_QUAL_RANGE"></span><span id="prop_qual_range"></span><dl> <dt>**intervallo di proprietà PROP \_ \_**</dt> </dl>                                   | Il valore numerico dovrebbe essere compreso in un intervallo specificato. Definire l'intervallo nel membro **lpRange** .<br/>                                                                                                                                                                                                                |
| <span id="PROP_QUAL_SET"></span><span id="prop_qual_set"></span><dl> <dt>**SET di proprietà PROP \_ \_**</dt> </dl>                                         | Il valore di una proprietà viene confrontato con un set di valori specificati nel membro **lpSet** dell'Unione della struttura. Il valore di una proprietà può essere un **byte**, una **parola**, un **DWORD**, un **largeInt** o un' **ora**.<br/>                                                                                                |
| <span id="PROP_QUAL_BITFIELD"></span><span id="prop_qual_bitfield"></span><dl> <dt>**PROP \_ qual \_ bit**</dt> </dl>                          | Obsoleta.<br/>                                                                                                                                                                                                                                                                                                            |
| <span id="PROP_QUAL_LABELED_SET"></span><span id="prop_qual_labeled_set"></span><dl> <dt>**\_set con \_ etichetta \_ set di prop**</dt> </dl>                | Il valore di una proprietà viene confrontato con un valore in un set di coppie di etichette di valore. Le coppie di etichette di valore vengono specificate nel membro **lpSet** dell'Unione della struttura. <br/> Al momento della visualizzazione, se il valore della proprietà corrisponde a un valore nel set, verranno visualizzati sia un valore che l'etichetta associata.<br/> |
| <span id="PROP_QUAL_LABELED_BITFIELD"></span><span id="prop_qual_labeled_bitfield"></span><dl> <dt>**PROP \_ qual \_ etichettato \_ bit**</dt> </dl> | Obsoleta. Usare invece i flag PROPa \_ \_ .<br/>                                                                                                                                                                                                                                                                             |
| <span id="PROP_QUAL_CONST"></span><span id="prop_qual_const"></span><dl> <dt>**PROP \_ qual \_ const**</dt> </dl>                                   | Il valore di una proprietà viene confrontato con una costante specificata nel membro **value** dell'Unione. <br/> In fase di visualizzazione, se i valori della proprietà e la costante non corrispondono, viene visualizzato un messaggio di errore formattato con il valore impostato come normale.<br/>                                                             |
| <span id="PROP_QUAL_FLAGS"></span><span id="prop_qual_flags"></span><dl> <dt>**flag di PROP \_ qual \_**</dt> </dl>                                   | Il valore della proprietà viene confrontato con i bit specifici identificati nel membro **lpSet** dell'Unione.<br/>                                                                                                                                                                                                              |
| <span id="PROP_QUAL_ARRAY"></span><span id="prop_qual_array"></span><dl> <dt>**\_Array prop qual \_**</dt> </dl>                                   | Il valore di una proprietà specifica una matrice di valori. La lunghezza dei dati associati determina la lunghezza di una matrice. <br/> Quando \_ \_ si imposta il valore della matrice prop, il membro Union della struttura dei dati **PROPERTYINFO** viene impostato su **null** e viene ignorato.<br/>                                                    |



 

</dd> <dt>

**lpExtendedInfo**
</dt> <dd>

Riservato (membro di Union).

</dd> <dt>

**lpRange**
</dt> <dd>

Puntatore a una struttura di [intervallo](range.md) che definisce un intervallo di valori. Questo membro deve essere impostato se il membro **dataqualifier** di questa struttura è impostato su Prop \_ qual \_ Range (membro di Union).

</dd> <dt>

**lpSet**
</dt> <dd>

Puntatore a una struttura di [set](set.md) che specifica un set di valori o di etichette. Questo membro deve essere impostato se il membro **dataqualifier** della struttura è impostato su Prop quale \_ \_ set, prop quale \_ \_ labeled \_ set o prop \_ qual \_ Flags (member of Union).

</dd> <dt>

**Maschera**
</dt> <dd>

Obsoleto (membro di Union).

</dd> <dt>

**Valore**
</dt> <dd>

Valore costante utilizzato quando **dataqualifier** è impostato su Prop \_ qual \_ const (membro di Union).

</dd> <dt>

**FormatStringSize**
</dt> <dd>

Dimensione massima utilizzata solo per la descrizione della proprietà.

</dd> <dt>

**InstanceData**
</dt> <dd>

Consente di specificare la funzione Format chiamata per formattare i dati visualizzati per la proprietà. Per utilizzare il formattatore generico, specificare la funzione **FormatPropertyInstance** .

</dd> </dl>

## <a name="remarks"></a>Commenti

La struttura **PROPERTYINFO** viene utilizzata nelle chiamate alla funzione [AddProperty](/previous-versions/bb251873(v=msdn.10)) . La funzione **AddProperty** aggiunge una singola definizione di proprietà al [*database della proprietà*](p.md)parser.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[AddProperty](/previous-versions/bb251873(v=msdn.10))
</dt> <dt>

[INTERVALLO](range.md)
</dt> <dt>

[SET](set.md)
</dt> </dl>

 

