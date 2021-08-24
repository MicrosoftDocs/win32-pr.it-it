---
description: Deprecato.
ms.assetid: eb2622bc-a98d-42bd-ab59-7a849000d79d
title: Funzione GetCalendarDateFormatEx
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
ms.openlocfilehash: db6bf4fc20c24e91a0af29dc8ee81f7a77ef5cb1c0f0e0f6c5a0a792e52eb903
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119068221"
---
# <a name="getcalendardateformatex-function"></a>Funzione GetCalendarDateFormatEx

Deprecato. Recupera una stringa di data formattata correttamente per le impostazioni locali specificate usando la data e il calendario specificati. L'utente può specificare il formato di data breve, il formato di data lunga, il formato del mese dell'anno o un modello di formato personalizzato.

> [!Note]  
> Questa funzione può recuperare i dati che cambiano tra le versioni, ad esempio a causa di impostazioni locali personalizzate. Se l'applicazione deve rendere persistenti o trasmettere dati, vedere [Uso dei dati delle impostazioni locali permanenti](using-persistent-locale-data.md).

 

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

*lpszLocale* \[ Pollici\]
</dt> <dd>

Puntatore a un nome di impostazioni locali o a uno dei valori predefiniti seguenti.

-   [\_ \_ INVARIANTE DEL NOME DELLE IMPOSTAZIONI LOCALI](locale-name-constants.md)
-   [IMPOSTAZIONI LOCALI \_ NOME \_ SISTEMA \_ PREDEFINITO](locale-name-constants.md)
-   [NOME \_ IMPOSTAZIONI LOCALI IMPOSTAZIONE PREDEFINITA \_ \_ DELL'UTENTE](locale-name-constants.md)

</dd> <dt>

*dwFlags* \[ Pollici\]
</dt> <dd>

Flag che specificano le opzioni di formato della data. Se *lpFormat* non è impostato su **NULL,** questo parametro deve essere impostato su 0. Se *lpFormat è* impostato su **NULL,** l'applicazione può specificare una combinazione dei valori seguenti e [LOCALE \_ NOUSEROVERRIDE](locale-nouseroverride.md).



| Valore                                                                                                                                                               | Significato                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span id="DATE_SHORTDATE"></span><span id="date_shortdate"></span><dl> <dt>**DATE \_ SHORTDATE**</dt> </dl>    | Usare il formato di data breve. Questo è il valore predefinito. Questo valore non può essere usato con DATE \_ LONGDATE o DATE \_ YEARMONTH. <br/> |
| <span id="DATE_LONGDATE"></span><span id="date_longdate"></span><dl> <dt>**DATE \_ LONGDATE**</dt> </dl>       | Usare il formato di data lunga. Questo valore non può essere usato con DATE \_ SHORTDATE o DATE \_ YEARMONTH. <br/>                      |
| <span id="DATE_YEARMONTH"></span><span id="date_yearmonth"></span><dl> <dt>**DATE \_ YEARMONTH**</dt> </dl>    | Usare il formato anno/mese. Questo valore non può essere usato con DATE \_ SHORTDATE o DATE \_ LONGDATE.<br/>                       |
| <span id="DATE_LTRREADING"></span><span id="date_ltrreading"></span><dl> <dt>**DATA \_ LTRREADING**</dt> </dl> | Aggiungere contrassegni per il layout di lettura da sinistra a destra. Questo valore non può essere usato con DATE \_ RTLREADING.<br/>                       |
| <span id="DATE_RTLREADING"></span><span id="date_rtlreading"></span><dl> <dt>**DATA \_ RTLREADING**</dt> </dl> | Aggiungere contrassegni per il layout di lettura da destra a sinistra. Questo valore non può essere usato con DATE \_ LTRREADING<br/>                        |



 

</dd> <dt>

*lpCalDateTime* \[ Pollici\]
</dt> <dd>

Puntatore a una [**struttura CALDATETIME**](caldatetime.md) che contiene le informazioni sulla data e sul calendario da formattare.

</dd> <dt>

*lpFormat* \[ Pollici\]
</dt> <dd>

Puntatore a una stringa dell'immagine di formato utilizzata per formare la stringa di data. I valori possibili per la stringa di formato dell'immagine sono definiti in [Day, Month, Year ed Era Format Pictures](day--month--year--and-era-format-pictures.md).

La stringa dell'immagine di formato deve essere con terminazione Null. La funzione usa le impostazioni locali solo per le informazioni non specificate nella stringa dell'immagine di formato, ad esempio i nomi dei giorni e dei mesi per le impostazioni locali. L'applicazione imposta questo parametro su **NULL** se la funzione deve usare il formato di data delle impostazioni locali specificate.

</dd> <dt>

*lpDateStr* \[ Cambio\]
</dt> <dd>

Puntatore a un buffer in cui questa funzione riceve la stringa di data formattata.

</dd> <dt>

*cchDate* \[ Pollici\]
</dt> <dd>

Dimensione, in caratteri, del buffer *lpDateStr.* In alternativa, l'applicazione può impostare questo parametro su 0. In questo caso, la funzione restituisce il numero di caratteri necessari per contenere la stringa di data formattata e il *parametro lpDateStr* non viene usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il numero di caratteri scritti nel buffer *lpDateStr* in caso di esito positivo. Se il *parametro cchDate* è impostato su 0, la funzione restituisce il numero di caratteri necessari per contenere la stringa di data formattata, incluso il carattere Null di terminazione.

Questa funzione restituisce 0 se non ha esito positivo. Per ottenere informazioni estese sull'errore, l'applicazione può chiamare [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), che può restituire uno dei codici di errore seguenti:

-   DATA \_ DI ERRORE NON COMPRESO \_ \_ \_ NELL'INTERVALLO. La data specificata non è in intervallo.
-   ERRORE \_ BUFFER \_ INSUFFICIENTE. Le dimensioni del buffer specificate non erano sufficienti o non erano impostate in modo errato su **NULL.**
-   ERRORE \_ FLAG NON \_ VALIDI. I valori forniti per i flag non sono validi.
-   ERRORE \_ PARAMETRO \_ NON VALIDO. Uno dei valori dei parametri non è valido.

## <a name="remarks"></a>Commenti

La data meno recente supportata da questa funzione è il 1° gennaio 1601.

A questa funzione non è associato un file di intestazione o un file di libreria. L'applicazione può chiamare [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) con il nome dll (Kernel32.dll) per ottenere un handle del modulo. Può quindi chiamare [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) con l'handle del modulo e il nome di questa funzione per ottenere l'indirizzo della funzione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                          |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Supporto linguistico nazionale](national-language-support.md)
</dt> <dt>

[Funzioni di supporto linguistico nazionale](national-language-support-functions.md)
</dt> <dt>

[Immagini in formato giorno, mese, anno ed era](day--month--year--and-era-format-pictures.md)
</dt> <dt>

[NLS: Esempio di API basate sui nomi](nls--name-based-apis-sample.md)
</dt> <dt>

[**EnumDateFormatsExEx**](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexex)
</dt> <dt>

[**GetDateFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformata)
</dt> <dt>

[**GetDateFormatEx**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformatex)
</dt> <dt>

[**CALDATETIME**](caldatetime.md)
</dt> </dl>

 

 
