---
description: Negli elenchi e nelle tabelle di questa sezione viene illustrato l'output del formattatore generico. Tenere presente che il formattatore generico usa i membri DataType e dataqualifier della struttura PROPERTYINFO per determinare come formattare i dati visualizzati.
ms.assetid: cf3dc6cd-7b24-464a-9d2b-5e35c4e8825e
title: Output formattatore generico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecf4b334dd717c7ff332c3b730afb57d4be611ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305919"
---
# <a name="generic-formatter-output"></a>Output formattatore generico

Negli elenchi e nelle tabelle di questa sezione viene illustrato l'output del [*formattatore generico*](g.md). Tenere presente che il formattatore generico usa i membri **DataType** e **dataqualifier** della struttura [**PROPERTYINFO**](propertyinfo.md) per determinare come formattare i dati visualizzati.

Per ulteriori informazioni e un esempio dell'output per un tipo di dati di proprietà specifico, vedere:

-   [\_tipo Prop \_ void](/windows)
-   [\_Riepilogo del tipo di Prop \_](/windows)
-   [tipo di PROP \_ \_ byte](/windows)
-   [tipo di PROP \_ \_ Word](/windows)
-   [tipo di PROP \_ \_ DWORD](/windows)
-   PROP \_ Type \_ largeInt (il formattatore generico non supporta)
-   \_Tipo Prop \_ addr (il formattatore generico non supporta)
-   [\_ora tipo di Prop \_](/windows)
-   [\_stringa di tipo Prop \_](/windows)
-   [\_ \_ indirizzo IP del tipo Prop \_](/windows)
-   PROP \_ Type \_ BYTESWAPPED \_ Word (obsoleto. Per altre informazioni, vedere [ \_ tipo Prop \_ Word](/windows))
-   PROP \_ Type \_ BYTESWAPPED \_ DWORD (obsoleto. Per altre informazioni, vedere [ \_ tipo Prop \_ DWORD](/windows))
-   \_Tipo Prop \_ stringa tipizzata \_ (obsoleto)
-   [tipi di PROP \_ \_ dati non elaborati \_](/windows)
-   [\_commento tipo \_ prop](/windows)
-   PROP \_ Type \_ SRCFRIENDLYNAME (il formattatore generico non supporta)
-   PROP \_ Type \_ DSTFRIENDLYNAME (il formattatore generico non supporta)
-   \_Indirizzo Tokenring di tipo Prop \_ \_ (il formattatore generico non supporta)
-   \_Indirizzo FDDI di tipo Prop \_ \_ (il formattatore generico non supporta)
-   \_Indirizzo Ethernet del tipo Prop \_ \_ (il formattatore generico non supporta)
-   \_Identificatore di oggetto di tipo Prop \_ \_ (il formattatore generico non supporta)
-   \_Indirizzo IP delle viti di tipo Prop \_ \_ \_ (il formattatore generico non supporta)
-   \_Tipo Prop \_ var \_ Len \_ small \_ int (il formattatore generico non supporta)

## <a name="prop_type_void-and-prop_type_comment"></a>Il \_ tipo Prop \_ void e il \_ tipo Prop \_ Comment

La tabella seguente elenca l'output di formato generico per le proprietà del tipo di dati del tipo di dati del tipo di oggetto **prop \_ \_ void** e **prop \_ \_** .

Nella colonna formattatore output il valore dei dati nell'acquisizione è XYZ.



| Qualificatore proprietà            | Output formattatore                                      |
|-------------------------------|-------------------------------------------------------|
| PROP \_ qual \_ None              | XYZ                                                   |
| intervallo di proprietà PROP \_ \_             | XYZ                                                   |
| PROP \_ qual \_ bit          | Obsoleti                                              |
| \_set con \_ etichetta \_ set di prop      | XYZ                                                   |
| PROP \_ qual \_ etichettato \_ bit | Obsoleta. Per ulteriori informazioni, vedere la pagina relativa ai \_ flag prop qual \_ |
| PROP \_ qual \_ const             | XYZ                                                   |
| flag di PROP \_ qual \_             | XYZ                                                   |
| \_Array prop qual \_             | XYZ                                                   |



 

## <a name="prop_type_summary"></a>\_Riepilogo del tipo di Prop \_

La tabella seguente elenca l'output di formato generico per le proprietà del tipo di dati di **\_ \_ Riepilogo del tipo prop** .

Nella colonna di output di esempio, il valore dei dati nell'acquisizione è XYZ.



| Qualificatore proprietà            | Output di esempio                                        |
|-------------------------------|-------------------------------------------------------|
| PROP \_ qual \_ None              | XYZ                                                   |
| intervallo di proprietà PROP \_ \_             | XYZ                                                   |
| PROP \_ qual \_ bit          | Obsoleti                                              |
| \_set con \_ etichetta \_ set di prop      | XYZ                                                   |
| PROP \_ qual \_ etichettato \_ bit | Obsoleta. Per ulteriori informazioni, vedere la pagina relativa ai \_ flag prop qual \_ |
| PROP \_ qual \_ const             | XYZ                                                   |
| flag di PROP \_ qual \_             | XYZ                                                   |
| \_Array prop qual \_             | XYZ                                                   |



 

## <a name="prop_type_byte"></a>tipo di PROP \_ \_ byte

La tabella seguente elenca l'output di formato generico per le proprietà del tipo di dati **\_ \_ byte di tipo prop** .

Nella colonna di output di esempio, il valore dei dati nell'acquisizione è 10.



| Qualificatore proprietà            | Output di esempio                                                                                                |
|-------------------------------|---------------------------------------------------------------------------------------------------------------|
| PROP \_ qual \_ None              | 10 (0xA) "                                                                                                     |
| intervallo di proprietà PROP \_ \_             | Intervallo di 10 (0xA):(1 (0x1)-20 (0x14))                                                                          |
| SET di proprietà PROP \_ \_               | 10 (0xA) corrisponde al valore impostato o<br/> 10 (0xA) valore impostato sconosciuto<br/>                                |
| PROP \_ qual \_ bit          | Obsoleta.                                                                                                     |
| \_set con \_ etichetta \_ set di prop      | Etichetta corrispondente in un set di etichette o un numero.                                                                 |
| PROP \_ qual \_ etichettato \_ bit | Obsoleta. Per ulteriori informazioni, vedere la pagina relativa ai \_ \_ flag prop.                                                        |
| PROP \_ qual \_ const             | Nessun output. Non vengono visualizzati dati nel riquadro dei dettagli.                                                           |
| flag di PROP \_ qual \_             | ....... 0 = etichetta fuori stringa...... 1. = Etichetta sulla stringa.... 0... = Etichetta fuori stringa... 1... = etichetta sulla stringa |
| \_Array prop qual \_             | 0A FF...                                                                                                     |



 

## <a name="prop_type_word"></a>tipo di PROP \_ \_ Word

La tabella seguente elenca l'output di formato generico per una proprietà tipo di dati **\_ \_ Word di tipo prop** .

> [!Note]  
> Per le proprietà DWORD con scambio di byte non Intel, è necessario modificare i dati in un formato Intel. Per modificare il formato, impostare il parametro *iFlags* della funzione di istanza della proprietà di **connessione** IFLAG \_ invertita quando si esegue il mapping dell'istanza di proprietà a un percorso.

 

Nella colonna di output di esempio, il valore dei dati nell'acquisizione è 10.



| Qualificatore proprietà            | Output di esempio                                                                                                                                                                                                                |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| PROP \_ qual \_ None              | 10 (0xA)                                                                                                                                                                                                                      |
| intervallo di proprietà PROP \_ \_             | Intervallo di 10 (0xA):(1 (0x1)-20 (0x14))                                                                                                                                                                                          |
| SET di proprietà PROP \_ \_               | 10 (0xA) corrisponde al valore impostato o<br/> 10 (0xA) valore impostato sconosciuto<br/>                                                                                                                                                |
| PROP \_ qual \_ bit          | Obsoleta.                                                                                                                                                                                                                     |
| \_set con \_ etichetta \_ set di prop      | Etichetta corrispondente nel set di etichette o nel numero.                                                                                                                                                                               |
| PROP \_ qual \_ etichettato \_ bit | Obsoleta. Per ulteriori informazioni, vedere la pagina relativa ai \_ \_ flag prop.                                                                                                                                                                        |
| PROP \_ qual \_ const             | Nessun output. Non vengono visualizzati dati nel riquadro dei dettagli.                                                                                                                                                                           |
| flag di PROP \_ qual \_             | ....... 0 = etichetta fuori stringa...... 0. = Etichetta fuori stringa.... 0... = Etichetta fuori stringa... 0... = etichetta fuori stringa... 0.... = etichetta off stringa.. 1..... = Etichetta su String. 0...... = Etichetta disattivato stringa 1....... = Etichetta sulla stringa |
| \_Array prop qual \_             | 000A FFFF...                                                                                                                                                                                                                 |



 

## <a name="prop_type_dword"></a>tipo di PROP \_ \_ DWORD

La tabella seguente elenca l'output di formato generico per le proprietà del tipo di dati **\_ \_ DWORD di tipo prop** .

> [!Note]  
> Per le proprietà DWORD con scambio di byte non Intel, è necessario modificare i dati in un formato Intel. Per modificare il formato, impostare il parametro *iFlags* della funzione di istanza della proprietà di **connessione** IFLAG \_ invertita quando si esegue il mapping dell'istanza di proprietà a un percorso.

 

Nella colonna di output di esempio, il valore dei dati nell'acquisizione è 10.



| Qualificatore proprietà            | Output di esempio                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|-------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| PROP \_ qual \_ None              | 10 (0xA)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| intervallo di proprietà PROP \_ \_             | Intervallo di 10 (0xA):(1 (0x1)-20 (0x14))                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| SET di proprietà PROP \_ \_               | 10 (0xA) corrisponde al valore impostato o<br/> 10 (0xA) valore impostato sconosciuto<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| PROP \_ qual \_ bit          | Obsoleta.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| \_set con \_ etichetta \_ set di prop      | Etichetta corrispondente nel set di etichette o nel numero.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| PROP \_ qual \_ etichettato \_ bit | Obsoleta. Per ulteriori informazioni, vedere la pagina relativa ai \_ \_ flag prop.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| PROP \_ qual \_ const             | Nessun output. Non vengono visualizzati dati nel riquadro dei dettagli.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| flag di PROP \_ qual \_             | ............... 0 = etichetta fuori stringa.............. 0. = Etichetta off stringa............. 0... = Etichetta off stringa............ 0... = etichetta off stringa........... 0.... = etichetta off stringa.......... 0..... = Etichetta off stringa......... 0...... = etichetta off stringa........ 0....... = etichetta off stringa....... 0....... = Etichetta fuori stringa...... 0......... = etichetta off stringa..... 0.......... = etichetta off stringa.... 0........... = Etichetta fuori stringa... 0............ = etichetta off stringa.. 1............. = etichetta su String. 0.............. = Etichetta off stringa 1............... = Etichetta sulla stringa |
| \_Array prop qual \_             | 0000000A FFFFFFFF...                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

## <a name="prop_type_raw_data"></a>tipi di PROP \_ \_ dati non elaborati \_

La tabella seguente elenca l'output di formato generico per una proprietà tipo di dati **\_ \_ RAW \_ data del tipo prop** . Tenere presente che l'output del formattatore non Visualizza i dati non elaborati, ma Visualizza l'etichetta della proprietà.



| Qualificatore proprietà            | Output formattatore |
|-------------------------------|------------------|
| PROP \_ qual \_ None              | Etichetta della proprietà.  |
| intervallo di proprietà PROP \_ \_             | Etichetta della proprietà.  |
| PROP \_ qual \_ bit          | Etichetta della proprietà.  |
| \_set con \_ etichetta \_ set di prop      | Etichetta della proprietà.  |
| PROP \_ qual \_ etichettato \_ bit | Etichetta della proprietà.  |
| PROP \_ qual \_ const             | Etichetta della proprietà.  |
| flag di PROP \_ qual \_             | Etichetta della proprietà.  |
| \_Array prop qual \_             | Etichetta della proprietà.  |



 

## <a name="prop_type_time"></a>\_ora tipo di Prop \_

La tabella seguente elenca l'output di formato generico per una proprietà tipo di dati **\_ \_ Time del tipo prop** . Tenere presente che l'output formattato può variare a seconda del qualificatore dati della proprietà.

Il formattatore generico chiama [**GetDateFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformata) per ottenere un'ora basata sull'orologio di sistema del computer locale.



| Qualificatore proprietà            | Output formattatore                                            |
|-------------------------------|-------------------------------------------------------------|
| PROP \_ qual \_ None              | Visualizza l'ora di sistema in base all'orologio del computer locale. |
| intervallo di proprietà PROP \_ \_             | Visualizza l'ora di sistema in base all'orologio del computer locale. |
| PROP \_ qual \_ bit          | Obsoleta.                                                   |
| \_set con \_ etichetta \_ set di prop      | Visualizza l'ora di sistema in base all'orologio del computer locale. |
| PROP \_ qual \_ etichettato \_ bit | Obsoleta. Per ulteriori informazioni, vedere la pagina relativa ai \_ \_ flag prop.      |
| PROP \_ qual \_ const             | Visualizza l'ora di sistema in base all'orologio del computer locale. |
| flag di PROP \_ qual \_             | Visualizza l'ora di sistema in base all'orologio del computer locale. |
| \_Array prop qual \_             | Visualizza l'ora di sistema in base all'orologio del computer locale. |



 

## <a name="prop_type_string"></a>\_stringa di tipo Prop \_

La tabella seguente elenca l'output di formato generico per le proprietà del tipo di dati **\_ \_ stringa di tipo prop** . Tenere presente che l'output del formattatore può variare a seconda del qualificatore dati della proprietà.



| Qualificatore proprietà            | Output formattatore                                       |
|-------------------------------|--------------------------------------------------------|
| PROP \_ qual \_ None              | Stringa collegata.                                       |
| intervallo di proprietà PROP \_ \_             | Stringa collegata.                                       |
| PROP \_ qual \_ bit          | Obsoleta.                                              |
| \_set con \_ etichetta \_ set di prop      | Stringa collegata.                                       |
| PROP \_ qual \_ etichettato \_ bit | Obsoleta. Per ulteriori informazioni, vedere la pagina relativa ai \_ \_ flag prop. |
| PROP \_ qual \_ const             | Stringa collegata.                                       |
| flag di PROP \_ qual \_             | Stringa collegata.                                       |
| \_Array prop qual \_             | Stringa collegata.                                       |



 

## <a name="prop_type_ip_address"></a>\_ \_ indirizzo IP del tipo Prop \_

La tabella seguente elenca l'output di formato generico per le proprietà del tipo di dati dell' **\_ \_ \_ indirizzo IP del tipo prop** . Tenere presente che l'output formattato può variare a seconda del qualificatore dei dati della proprietà.

Nella colonna di output di esempio, il valore dei dati nell'acquisizione è "129.65.100.2".



| Qualificatore proprietà            | Output di esempio                                         |
|-------------------------------|--------------------------------------------------------|
| PROP \_ qual \_ None              | 129.65.100.2                                           |
| intervallo di proprietà PROP \_ \_             | 129.65.100.2                                           |
| PROP \_ qual \_ bit          | Obsoleta.                                              |
| \_set con \_ etichetta \_ set di prop      | 129.65.100.2                                           |
| PROP \_ qual \_ etichettato \_ bit | Obsoleta. Per ulteriori informazioni, vedere la pagina relativa ai \_ \_ flag prop. |
| PROP \_ qual \_ const             | 129.65.100.2                                           |
| flag di PROP \_ qual \_             | 129.65.100.2                                           |
| \_Array prop qual \_             | 129.65.100.2                                           |



 

 

