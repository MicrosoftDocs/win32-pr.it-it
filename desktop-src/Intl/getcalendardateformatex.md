---
description: Deprecato.
ms.assetid: eb2622bc-a98d-42bd-ab59-7a849000d79d
title: GetCalendarDateFormatEx (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCalendarDateFormatEx
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-calendar-l1-1-0.dll
- kernel32legacy.dll
ms.openlocfilehash: b0130bf62c742d0565b1c98c138ac8c71ddf7a67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312873"
---
# <a name="getcalendardateformatex-function"></a>GetCalendarDateFormatEx (funzione)

Deprecato. Recupera una stringa di data formattata correttamente per le impostazioni locali specificate utilizzando la data e il calendario specificati. L'utente può specificare il formato di data breve, il formato di data estesa, il formato dell'anno mese o un modello di formato personalizzato.

> [!Note]  
> Questa funzione può recuperare i dati che cambiano tra le versioni, ad esempio, a causa di impostazioni locali personalizzate. Se l'applicazione deve persistere o trasmettere dati, vedere [utilizzo di dati locali permanenti](using-persistent-locale-data.md).

 

## <a name="syntax"></a>Sintassi


```C++
BOOL GetCalendarDateFormatEx(
  _In_        LPCWSTR       lpszLocale,
  _In_        DWORD         dwFlags,
  _In_  const LPCALDATETIME lpCalDateTime,
  _In_        LPCWSTR       lpFormat,
  _Out_       LPWSTR        lpDateStr,
  _In_        int           cchDate
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lpszLocale* \[ in\]
</dt> <dd>

Puntatore a un nome delle impostazioni locali o uno dei seguenti valori predefiniti.

-   [nome delle impostazioni locali \_ \_ invariante](locale-name-constants.md)
-   [impostazioni locali \_ nome \_ sistema \_ predefinito](locale-name-constants.md)
-   [\_ \_ impostazione predefinita utente nome impostazioni locali \_](locale-name-constants.md)

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Flag che specificano le opzioni relative al formato della data. Se *lpFormat* non è impostato su **null**, questo parametro deve essere impostato su 0. Se *lpFormat* è impostato su **null**, l'applicazione può specificare una combinazione dei valori seguenti e delle [impostazioni locali \_ NOUSEROVERRIDE](locale-nouseroverride.md).



| Valore                                                                                                                                                               | Significato                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span id="DATE_SHORTDATE"></span><span id="date_shortdate"></span><dl> <dt>**Data \_ SHORTDATE**</dt> </dl>    | Usare il formato di data breve. Questo è il valore predefinito. Questo valore non può essere usato con la data \_ LONGDATE o la data \_ YEARMONTH. <br/> |
| <span id="DATE_LONGDATE"></span><span id="date_longdate"></span><dl> <dt>**Data \_ LONGDATE**</dt> </dl>       | Usare il formato di data estesa. Questo valore non può essere usato con la data \_ shortdate o la data \_ YEARMONTH. <br/>                      |
| <span id="DATE_YEARMONTH"></span><span id="date_yearmonth"></span><dl> <dt>**Data \_ YEARMONTH**</dt> </dl>    | Usare il formato anno/mese. Questo valore non può essere usato con la data \_ shortdate o la data \_ LONGDATE.<br/>                       |
| <span id="DATE_LTRREADING"></span><span id="date_ltrreading"></span><dl> <dt>**Data \_ LTRREADING**</dt> </dl> | Aggiungere i contrassegni per il layout di lettura da sinistra a destra. Questo valore non può essere usato con la data \_ RTLREADING.<br/>                       |
| <span id="DATE_RTLREADING"></span><span id="date_rtlreading"></span><dl> <dt>**Data \_ RTLREADING**</dt> </dl> | Aggiungere contrassegni per il layout di lettura da destra a sinistra. Non è possibile usare questo valore con DATE \_ LTRREADING<br/>                        |



 

</dd> <dt>

*lpCalDateTime* \[ in\]
</dt> <dd>

Puntatore a una struttura [**CALDATETIME**](caldatetime.md) che contiene le informazioni sulla data e sul calendario da formattare.

</dd> <dt>

*lpFormat* \[ in\]
</dt> <dd>

Puntatore a una stringa di immagine del formato utilizzata per formare la stringa di data. I valori possibili per la stringa dell'immagine di formato sono definiti nelle [Immagini del formato giorno, mese, anno ed era](day--month--year--and-era-format-pictures.md).

La stringa di formato dell'immagine deve essere con terminazione null. La funzione utilizza le impostazioni locali solo per le informazioni non specificate nella stringa dell'immagine di formato, ad esempio i nomi dei giorni e dei mesi per le impostazioni locali. Se la funzione usa il formato di data delle impostazioni locali specificate, l'applicazione imposta questo parametro su **null** .

</dd> <dt>

*lpDateStr* \[ out\]
</dt> <dd>

Puntatore a un buffer in cui questa funzione riceve la stringa di data formattata.

</dd> <dt>

*cchDate* \[ in\]
</dt> <dd>

Dimensione, in caratteri, del buffer *lpDateStr* . In alternativa, l'applicazione può impostare questo parametro su 0. In questo caso, la funzione restituisce il numero di caratteri necessari per conservare la stringa di data formattata e il parametro *lpDateStr* non viene utilizzato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il numero di caratteri scritti nel buffer *lpDateStr* in caso di esito positivo. Se il parametro *cchDate* è impostato su 0, la funzione restituisce il numero di caratteri necessari per conservare la stringa di data formattata, incluso il carattere null di terminazione.

Questa funzione restituisce 0 in caso di esito negativo. Per ottenere informazioni estese sull'errore, l'applicazione può chiamare [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), che può restituire uno dei codici di errore seguenti:

-   \_Data di errore non \_ compresa nell' \_ \_ intervallo. La data specificata non è compresa nell'intervallo.
-   ERRORE \_ \_ nel buffer insufficiente. Una dimensione del buffer specificata non è sufficientemente grande oppure è stata impostata erroneamente su **null**.
-   flag di errore \_ non validi \_ . I valori specificati per i flag non sono validi.
-   ERRORE \_ parametro non valido \_ . Uno dei valori di parametro non è valido.

## <a name="remarks"></a>Commenti

La data meno recente supportata da questa funzione è il 1 gennaio 1601.

A questa funzione non è associato un file di intestazione o un file di libreria. L'applicazione può chiamare [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) con il nome della DLL (Kernel32.dll) per ottenere un handle del modulo. Può quindi chiamare [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) con tale handle del modulo e il nome di questa funzione per ottenere l'indirizzo della funzione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Supporto per lingua nazionale](national-language-support.md)
</dt> <dt>

[Funzioni di supporto del linguaggio nazionale](national-language-support-functions.md)
</dt> <dt>

[Immagini del formato giorno, mese, anno ed era](day--month--year--and-era-format-pictures.md)
</dt> <dt>

[NLS: esempio di API basate su nome](nls--name-based-apis-sample.md)
</dt> <dt>

[**EnumDateFormatsExEx**](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexex)
</dt> <dt>

[**GetDateFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformata)
</dt> <dt>

[**GetDateFormatEx**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformatex)
</dt> <dt>

[**CALDATETIME**](caldatetime.md)
</dt> </dl>

 

 
