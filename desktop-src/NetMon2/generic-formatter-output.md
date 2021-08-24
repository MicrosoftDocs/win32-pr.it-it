---
description: Gli elenchi e le tabelle in questa sezione mostrano l'output del formattatore generico. Tenere presente che il formattatore generico usa i membri DataType e DataQualifier della struttura PROPERTYINFO per determinare come formattare i dati visualizzati.
ms.assetid: cf3dc6cd-7b24-464a-9d2b-5e35c4e8825e
title: Output del formattatore generico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d76a67fadbed3bde5eb3e5534c8f104e918ac870df27c767b98575058a0a188
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119743971"
---
# <a name="generic-formatter-output"></a>Output del formattatore generico

Gli elenchi e le tabelle in questa sezione mostrano l'output del [*formattatore generico*](g.md). Tenere presente che il formattatore generico usa i **membri DataType** e **DataQualifier** della [**struttura PROPERTYINFO**](propertyinfo.md) per determinare come formattare i dati visualizzati.

Per altre informazioni e un esempio dell'output per un tipo di dati di proprietà specifico, vedere:

-   [PROP \_ TYPE \_ VOID](/windows)
-   [RIEPILOGO \_ DEL TIPO DI \_ PROPRIETÀ](/windows)
-   [PROP \_ TYPE \_ BYTE](/windows)
-   [PROP \_ TYPE \_ WORD](/windows)
-   [PROP \_ TYPE \_ DWORD](/windows)
-   PROP \_ TYPE \_ LARGEINT (il formattatore generico non supporta)
-   PROP \_ TYPE \_ ADDR (il formattatore generico non supporta)
-   [PROP \_ TYPE \_ TIME](/windows)
-   [PROP \_ TYPE \_ STRING](/windows)
-   [INDIRIZZO \_ IP DI TIPO \_ \_ PROP](/windows)
-   TIPO PROP \_ \_ BYTESWAPPED \_ WORD (obsoleto. Per altre informazioni, vedere [PROP \_ TYPE \_ WORD](/windows))
-   TIPO \_ PROP \_ BYTESWAPPED \_ DWORD (obsoleto. Per altre informazioni, vedere [PROP \_ TYPE \_ DWORD](/windows))
-   PROP \_ TYPE \_ TYPED STRING \_ (Obsolete)
-   [DATI NON \_ ELABORATI \_ DI TIPO \_ PROP](/windows)
-   [PROP \_ TYPE \_ COMMENT](/windows)
-   PROP \_ TYPE \_ SRCFRIENDLYNAME (il formattatore generico non supporta)
-   PROP \_ TYPE \_ DSTFRIENDLYNAME (il formattatore generico non supporta)
-   PROP \_ TYPE \_ TOKENRING ADDRESS \_ (il formattatore generico non supporta)
-   PROP \_ TYPE \_ FDDI \_ ADDRESS (il formattatore generico non supporta)
-   PROP \_ TYPE \_ INDIRIZZO ETHERNET \_ (il formattatore generico non supporta)
-   PROP \_ TYPE OBJECT IDENTIFIER \_ \_ (il formattatore generico non supporta)
-   PROP \_ TYPE \_ VINES IP ADDRESS \_ \_ (il formattatore generico non supporta)
-   PROP \_ TYPE \_ VAR \_ LEN SMALL INT \_ \_ (il formattatore generico non supporta)

## <a name="prop_type_void-and-prop_type_comment"></a>PROP \_ TYPE VOID e PROP TYPE \_ \_ \_ COMMENT

Nella tabella seguente viene elencato l'output di formato generico per le proprietà dei tipi di dati **PROP \_ TYPE \_ VOID** e **PROP TYPE \_ \_ COMMENT.**

Nella colonna di output del formattatore il valore dei dati nell'acquisizione è XYZ.



| Qualificatore proprietà            | Output del formattatore                                      |
|-------------------------------|-------------------------------------------------------|
| PROP \_ QUAL \_ NONE              | XYZ                                                   |
| PROP \_ QUAL \_ RANGE             | XYZ                                                   |
| PROP \_ QUAL \_ BITFIELD          | Obsoleti                                              |
| PROP \_ QUAL \_ LABELED \_ SET      | XYZ                                                   |
| CAMPO \_ DI BIT CON \_ ETICHETTA \_ PROP QUAL | Obsoleta. Per altre informazioni, vedere FLAG PROP \_ QUAL \_ |
| PROP \_ QUAL \_ CONST             | XYZ                                                   |
| FLAG PROP \_ QUAL \_             | XYZ                                                   |
| PROP \_ QUAL \_ ARRAY             | XYZ                                                   |



 

## <a name="prop_type_summary"></a>RIEPILOGO \_ DEL TIPO DI \_ PROPRIETÀ

Nella tabella seguente viene elencato l'output di formato generico per le proprietà del tipo di dati **\_ PROP TYPE \_ SUMMARY.**

Nella colonna di output di esempio il valore dei dati nell'acquisizione è XYZ.



| Qualificatore proprietà            | Output di esempio                                        |
|-------------------------------|-------------------------------------------------------|
| PROP \_ QUAL \_ NONE              | XYZ                                                   |
| PROP \_ QUAL \_ RANGE             | XYZ                                                   |
| PROP \_ QUAL \_ BITFIELD          | Obsoleti                                              |
| PROP \_ QUAL \_ LABELED \_ SET      | XYZ                                                   |
| CAMPO \_ DI BIT CON \_ ETICHETTA \_ PROP QUAL | Obsoleta. Per altre informazioni, vedere FLAG PROP \_ QUAL \_ |
| PROP \_ QUAL \_ CONST             | XYZ                                                   |
| FLAG PROP \_ QUAL \_             | XYZ                                                   |
| PROP \_ QUAL \_ ARRAY             | XYZ                                                   |



 

## <a name="prop_type_byte"></a>PROP \_ TYPE \_ BYTE

Nella tabella seguente viene elencato l'output di formato generico per le proprietà del tipo di dati **PROP \_ TYPE \_ BYTE.**

Nella colonna di output di esempio il valore dei dati nell'acquisizione è 10.



| Qualificatore proprietà            | Output di esempio                                                                                                |
|-------------------------------|---------------------------------------------------------------------------------------------------------------|
| PROP \_ QUAL \_ NONE              | 10 (0xa)"                                                                                                     |
| PROP \_ QUAL \_ RANGE             | 10 (0xa) Range:(1 (0x1) - 20 (0x14))                                                                          |
| PROP \_ QUAL \_ SET               | 10 (0xa) corrisponde al valore impostato o<br/> 10 (0xa) Unknown Set Value<br/>                                |
| PROP \_ QUAL \_ BITFIELD          | Obsoleta.                                                                                                     |
| PROP \_ QUAL \_ LABELED \_ SET      | Etichetta corrispondente in un set di etichette o in un numero.                                                                 |
| CAMPO \_ DI BIT CON \_ ETICHETTA \_ PROP QUAL | Obsoleta. Per altre informazioni, vedere FLAG PROP \_ \_ QUAL.                                                        |
| PROP \_ QUAL \_ CONST             | Nessun output. Nel riquadro dei dettagli non viene visualizzato alcun dato.                                                           |
| FLAG PROP \_ QUAL \_             | ....... 0 = Label Off String ...... 1. = Etichetta sulla stringa ..... 0.. = Label Off String .... 1... = Etichetta su stringa |
| PROP \_ QUAL \_ ARRAY             | 0a ff ...                                                                                                     |



 

## <a name="prop_type_word"></a>PROP \_ TYPE \_ WORD

Nella tabella seguente viene elencato l'output di formato generico per una proprietà del tipo di dati **\_ PROP TYPE \_ WORD.**

> [!Note]  
> Per le proprietà DWORD non Intel scambiate con byte, è necessario modificare i dati in un formato Intel. Per modificare il formato, impostare il *parametro IFlags* della funzione di istanza della proprietà **Attach** IFLAG SWAPPED quando si esegue il mapping dell'istanza della proprietà \_ a una posizione.

 

Nella colonna di output di esempio il valore dei dati nell'acquisizione è 10.



| Qualificatore proprietà            | Output di esempio                                                                                                                                                                                                                |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| PROP \_ QUAL \_ NONE              | 10 (0xa)                                                                                                                                                                                                                      |
| PROP \_ QUAL \_ RANGE             | 10 (0xa) Range:(1 (0x1) - 20 (0x14))                                                                                                                                                                                          |
| PROP \_ QUAL \_ SET               | 10 (0xa) corrisponde al valore impostato o<br/> 10 (0xa) Unknown Set Value<br/>                                                                                                                                                |
| PROP \_ QUAL \_ BITFIELD          | Obsoleta.                                                                                                                                                                                                                     |
| PROP \_ QUAL \_ LABELED \_ SET      | Etichetta corrispondente nel set di etichette o nel numero.                                                                                                                                                                               |
| CAMPO \_ DI BIT CON \_ ETICHETTA \_ PROP QUAL | Obsoleta. Per altre informazioni, vedere FLAG PROP \_ \_ QUAL.                                                                                                                                                                        |
| PROP \_ QUAL \_ CONST             | Nessun output. Nel riquadro dei dettagli non viene visualizzato alcun dato.                                                                                                                                                                           |
| FLAG PROP \_ QUAL \_             | ....... 0 = Label Off String ...... 0. = Label Off String ..... 0.. = Label Off String .... 0... = Label Off String ... 0.... = Label Off String .. 1..... = Etichetta sulla stringa .0...... = Label Off String 1....... = Etichetta su stringa |
| PROP \_ QUAL \_ ARRAY             | 000a ffff ...                                                                                                                                                                                                                 |



 

## <a name="prop_type_dword"></a>PROP \_ TYPE \_ DWORD

Nella tabella seguente viene elencato l'output di formato generico per le proprietà del tipo di dati **\_ \_ DWORD PROP TYPE.**

> [!Note]  
> Per le proprietà DWORD non Intel scambiate con byte, è necessario modificare i dati in un formato Intel. Per modificare il formato, impostare il *parametro IFlags* della funzione di istanza della proprietà **Attach** IFLAG SWAPPED quando si esegue il mapping dell'istanza della proprietà \_ a una posizione.

 

Nella colonna di output di esempio il valore dei dati nell'acquisizione è 10.



| Qualificatore proprietà            | Output di esempio                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|-------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| PROP \_ QUAL \_ NONE              | 10 (0xa)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| PROP \_ QUAL \_ RANGE             | 10 (0xa) Range:(1 (0x1) - 20 (0x14))                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| PROP \_ QUAL \_ SET               | 10 (0xa) corrisponde al valore impostato o<br/> 10 (0xa) Unknown Set Value<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| PROP \_ QUAL \_ BITFIELD          | Obsoleta.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| PROP \_ QUAL \_ LABELED \_ SET      | Etichetta corrispondente nel set di etichette o nel numero.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| CAMPO \_ DI BIT CON \_ ETICHETTA \_ PROP QUAL | Obsoleta. Per altre informazioni, vedere FLAG PROP \_ \_ QUAL.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| PROP \_ QUAL \_ CONST             | Nessun output. Nel riquadro dei dettagli non viene visualizzato alcun dato.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| FLAG PROP \_ QUAL \_             | ............... 0 = Label Off String .............. 0. = Label Off String ............. 0.. = Label Off String ............ 0... = Label Off String ........... 0.... = Label Off String .......... 0..... = Label Off String ......... 0...... = Label Off String ........ 0....... = Label Off String ....... 0........ = Label Off String ...... 0......... = Label Off String ..... 0.......... = Label Off String .... 0........... = Label Off String ... 0............ = Label Off String .. 1............. = Etichetta sulla stringa .0.............. = Label Off String 1.................. = Etichetta su stringa |
| PROP \_ QUAL \_ ARRAY             | 0000000a ffffffff ...                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

## <a name="prop_type_raw_data"></a>DATI NON \_ ELABORATI \_ DI TIPO \_ PROP

Nella tabella seguente viene elencato l'output di formato generico per una proprietà del tipo di dati **RAW DATA DI \_ \_ TIPO \_ PROP.** Tenere presente che l'output del formattatore non visualizza i dati non elaborati, ma visualizza l'etichetta della proprietà.



| Qualificatore proprietà            | Output del formattatore |
|-------------------------------|------------------|
| PROP \_ QUAL \_ NONE              | Etichetta della proprietà.  |
| PROP \_ QUAL \_ RANGE             | Etichetta della proprietà.  |
| PROP \_ QUAL \_ BITFIELD          | Etichetta della proprietà.  |
| PROP \_ QUAL \_ LABELED \_ SET      | Etichetta della proprietà.  |
| CAMPO \_ DI BIT CON \_ ETICHETTA \_ PROP QUAL | Etichetta della proprietà.  |
| PROP \_ QUAL \_ CONST             | Etichetta della proprietà.  |
| FLAG PROP \_ QUAL \_             | Etichetta della proprietà.  |
| PROP \_ QUAL \_ ARRAY             | Etichetta della proprietà.  |



 

## <a name="prop_type_time"></a>PROP \_ TYPE \_ TIME

Nella tabella seguente viene elencato l'output di formato generico per una proprietà del tipo di dati **\_ PROP TYPE \_ TIME.** Tenere presente che l'output formattato può variare a seconda del qualificatore di dati della proprietà .

Il formattatore generico [**chiama GetDateFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformata) per ottenere un'ora basata sull'orologio di sistema del computer locale.



| Qualificatore proprietà            | Output del formattatore                                            |
|-------------------------------|-------------------------------------------------------------|
| PROP \_ QUAL \_ NONE              | Visualizza l'ora di sistema in base all'orologio del computer locale. |
| PROP \_ QUAL \_ RANGE             | Visualizza l'ora di sistema in base all'orologio del computer locale. |
| PROP \_ QUAL \_ BITFIELD          | Obsoleta.                                                   |
| PROP \_ QUAL \_ LABELED \_ SET      | Visualizza l'ora di sistema in base all'orologio del computer locale. |
| CAMPO \_ DI BIT CON \_ ETICHETTA \_ PROP QUAL | Obsoleta. Per altre informazioni, vedere FLAG PROP \_ \_ QUAL.      |
| PROP \_ QUAL \_ CONST             | Visualizza l'ora di sistema in base all'orologio del computer locale. |
| FLAG PROP \_ QUAL \_             | Visualizza l'ora di sistema in base all'orologio del computer locale. |
| PROP \_ QUAL \_ ARRAY             | Visualizza l'ora di sistema in base all'orologio del computer locale. |



 

## <a name="prop_type_string"></a>PROP \_ TYPE \_ STRING

Nella tabella seguente viene elencato l'output di formato generico per le proprietà del tipo di dati **\_ PROP TYPE \_ STRING.** Tenere presente che l'output del formattatore può variare a seconda del qualificatore di dati della proprietà.



| Qualificatore proprietà            | Output del formattatore                                       |
|-------------------------------|--------------------------------------------------------|
| PROP \_ QUAL \_ NONE              | Stringa associata.                                       |
| PROP \_ QUAL \_ RANGE             | Stringa associata.                                       |
| PROP \_ QUAL \_ BITFIELD          | Obsoleta.                                              |
| PROP \_ QUAL \_ LABELED \_ SET      | Stringa associata.                                       |
| CAMPO \_ DI BIT CON \_ ETICHETTA \_ PROP QUAL | Obsoleta. Per altre informazioni, vedere FLAG PROP \_ \_ QUAL. |
| PROP \_ QUAL \_ CONST             | Stringa associata.                                       |
| FLAG PROP \_ QUAL \_             | Stringa associata.                                       |
| PROP \_ QUAL \_ ARRAY             | Stringa associata.                                       |



 

## <a name="prop_type_ip_address"></a>INDIRIZZO \_ IP DI TIPO \_ \_ PROP

Nella tabella seguente viene elencato l'output di formato generico per le proprietà del tipo di dati **\_ \_ \_ INDIRIZZO IP** TIPO PROP. Tenere presente che l'output formattato può variare a seconda del qualificatore di dati della proprietà.

Nella colonna di output di esempio il valore dei dati nell'acquisizione è "129.65.100.2".



| Qualificatore proprietà            | Output di esempio                                         |
|-------------------------------|--------------------------------------------------------|
| PROP \_ QUAL \_ NONE              | 129.65.100.2                                           |
| PROP \_ QUAL \_ RANGE             | 129.65.100.2                                           |
| PROP \_ QUAL \_ BITFIELD          | Obsoleta.                                              |
| PROP \_ QUAL \_ LABELED \_ SET      | 129.65.100.2                                           |
| CAMPO \_ DI BIT CON \_ ETICHETTA \_ PROP QUAL | Obsoleta. Per altre informazioni, vedere FLAG PROP \_ \_ QUAL. |
| PROP \_ QUAL \_ CONST             | 129.65.100.2                                           |
| FLAG PROP \_ QUAL \_             | 129.65.100.2                                           |
| PROP \_ QUAL \_ ARRAY             | 129.65.100.2                                           |



 

 

