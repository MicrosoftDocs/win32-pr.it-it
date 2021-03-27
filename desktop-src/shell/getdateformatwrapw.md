---
description: Formatta una data come stringa di data per le impostazioni locali specificate.
ms.assetid: e45f6d1c-2890-44f6-8406-022c99c59e02
title: GetDateFormatWrapW (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetDateFormatWrapW
api_type:
- DllExport
api_location:
- Shlwapi.dll
ms.openlocfilehash: c9c369584fd15a27d5e684452b2277104b5b1da4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227442"
---
# <a name="getdateformatwrapw-function"></a>GetDateFormatWrapW (funzione)

\[**GetDateFormatWrapW** è disponibile per l'utilizzo in Windows XP. Non sarà disponibile nelle versioni successive. È consigliabile usare [**GetDateFormatW**](/windows/win32/api/datetimeapi/nf-datetimeapi-getdateformata) al suo posto.\]

Formatta una data come stringa di data per le impostazioni locali specificate. La funzione formatta una data specificata o una data di sistema locale.

> [!Note]  
> **GetDateFormatWrapW** è un wrapper per la funzione **GetDateFormatW** . Per ulteriori note sull'utilizzo, vedere la pagina [**GetDateFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-getdateformata) .

 

## <a name="syntax"></a>Sintassi


```C++
int GetDateFormatWrapW(
  _In_        LCID       Locale,
  _In_        DWORD      dwFlags,
  _In_  const SYSTEMTIME *lpDate,
  _In_        LPCWSTR    pwzFormat,
  _Out_       LPWSTR     pwzDateStr,
  _In_        int        cchDate
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Impostazioni locali* \[ in\]
</dt> <dd>

Tipo: **LCID**

Impostazioni locali per cui deve essere formattata la stringa di data. Se *pwzFormat* è **null**, la funzione formatta la stringa in base al formato della data per le impostazioni locali. Se *pwzFormat* non è **null**, la funzione usa le impostazioni locali solo per le informazioni non specificate nella stringa dell'immagine di formato (ad esempio, i nomi di giorno e mese delle impostazioni locali).

Questo parametro può essere un identificatore delle impostazioni locali creato dalla macro [**MAKELCID**](/windows/win32/api/winnt/nf-winnt-makelcid) o uno dei seguenti valori predefiniti.

<dt>

<span id="LOCALE_SYSTEM_DEFAULT"></span><span id="locale_system_default"></span>

<span id="LOCALE_SYSTEM_DEFAULT"></span><span id="locale_system_default"></span>**impostazioni locali del \_ sistema \_**


</dt> <dd>

Impostazioni locali del sistema predefinite.

</dd> <dt>

<span id="LOCALE_USER_DEFAULT"></span><span id="locale_user_default"></span>

<span id="LOCALE_USER_DEFAULT"></span><span id="locale_user_default"></span>**\_impostazione predefinita utente impostazioni locali \_**


</dt> <dd>

Impostazioni locali dell'utente predefinite.

</dd> </dl> </dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Tipo: **DWORD**

Specifica varie opzioni di funzione. Se *pwzFormat* non è **null**, questo parametro deve essere zero. Se *pwzFormat* è **null**, è possibile specificare una combinazione dei valori seguenti. Se non si specifica data \_ YEARMONTH, date \_ shortdate o date \_ LONGDATE e *pwzFormat* è **null**, \_ viene utilizzata la data shortdate come valore predefinito.

<dt>

<span id="LOCALE_NOUSEROVERRIDE"></span><span id="locale_nouseroverride"></span>

<span id="LOCALE_NOUSEROVERRIDE"></span><span id="locale_nouseroverride"></span>**impostazioni locali \_ NOUSEROVERRIDE**


</dt> <dd>

Se impostata, la funzione formatta la stringa utilizzando il formato di data predefinito del sistema per le impostazioni locali specificate. Se non è impostato, la funzione formatta la stringa usando qualsiasi override utente nel formato di data predefinito delle impostazioni locali.

</dd> <dt>

<span id="LOCALE_USE_CP_ACP"></span><span id="locale_use_cp_acp"></span>

<span id="LOCALE_USE_CP_ACP"></span><span id="locale_use_cp_acp"></span>**impostazioni locali \_ usare \_ CP \_ ACP**


</dt> <dd>

Usa la tabella codici ANSI di sistema per la conversione di stringhe anziché la tabella codici delle impostazioni locali.

</dd> <dt>

<span id="DATE_SHORTDATE"></span><span id="date_shortdate"></span>

<span id="DATE_SHORTDATE"></span><span id="date_shortdate"></span>**Data \_ SHORTDATE**


</dt> <dd>

Usa il formato di data breve. Questo valore non può essere usato con la data \_ LONGDATE o la data \_ YEARMONTH.

</dd> <dt>

<span id="DATE_LONGDATE"></span><span id="date_longdate"></span>

<span id="DATE_LONGDATE"></span><span id="date_longdate"></span>**Data \_ LONGDATE**


</dt> <dd>

Usa il formato di data estesa. Questo valore non può essere usato con la data \_ shortdate o la data \_ YEARMONTH.

</dd> <dt>

<span id="DATE_YEARMONTH"></span><span id="date_yearmonth"></span>

<span id="DATE_YEARMONTH"></span><span id="date_yearmonth"></span>**Data \_ YEARMONTH**


</dt> <dd>

Usa il formato anno/mese. Questo valore non può essere usato con la data \_ shortdate o la data \_ LONGDATE.

</dd> <dt>

<span id="DATE_USE_ALT_CALENDAR"></span><span id="date_use_alt_calendar"></span>

<span id="DATE_USE_ALT_CALENDAR"></span><span id="date_use_alt_calendar"></span>**Data \_ utilizzo \_ ALT \_ Calendario**


</dt> <dd>

Usa il calendario alternativo, se esistente, per formattare la stringa di data. Se questo flag è impostato, la funzione utilizza il formato predefinito per quel calendario alternativo, anziché utilizzare qualsiasi override utente. Le sostituzioni utente verranno utilizzate solo nel caso in cui non esista un formato predefinito per il calendario alternativo specificato.

</dd> <dt>

<span id="DATE_LTRREADING"></span><span id="date_ltrreading"></span>

<span id="DATE_LTRREADING"></span><span id="date_ltrreading"></span>**Data \_ LTRREADING**


</dt> <dd>

Aggiunge contrassegni per il layout di lettura da sinistra a destra. Questo valore non può essere usato con la data \_ RTLREADING.

</dd> <dt>

<span id="DATE_RTLREADING"></span><span id="date_rtlreading"></span>

<span id="DATE_RTLREADING"></span><span id="date_rtlreading"></span>**Data \_ RTLREADING**


</dt> <dd>

Aggiunge contrassegni per il layout di lettura da destra a sinistra. Questo valore non può essere usato con la data \_ LTRREADING.

</dd> </dl> </dd> <dt>

*lpDate* \[ in\]
</dt> <dd>

Tipo: **const [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) \** _

Puntatore a una struttura [_ *SYSTEMTIME* *](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) che contiene le informazioni sulla data da formattare. Se questo puntatore è **null**, la funzione usa la data corrente del sistema locale.

</dd> <dt>

*pwzFormat* \[ in\]
</dt> <dd>

Tipo: **LPCWSTR**

Puntatore a un'immagine di formato da utilizzare per formare la stringa di data. Se *pwzFormat* è **null**, la funzione utilizza il formato di data delle impostazioni locali specificate. Per ulteriori informazioni, vedere [**GetDateFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-getdateformata) .

</dd> <dt>

*pwzDateStr* \[ out\]
</dt> <dd>

Tipo: **LPWSTR**

Puntatore a un buffer che riceve la stringa di data formattata.

</dd> <dt>

*cchDate* \[ in\]
</dt> <dd>

Tipo: **int**

Specifica la dimensione, in caratteri, del buffer *pwzDateStr* . Se *cchDate* è zero, la funzione restituisce il numero di caratteri necessari per memorizzare la stringa di data formattata e il buffer a cui punta *pwzDateStr* non viene utilizzato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **int**

Se la funzione ha esito positivo, il valore restituito è il numero di caratteri scritti nel buffer a cui punta *pwzDateStr*. Se il parametro *cchDate* è zero, il valore restituito è il numero di caratteri necessari per conservare la stringa di data formattata. Il conteggio include il carattere null di terminazione.

Se la funzione ha esito negativo, il valore restituito è zero. Per informazioni dettagliate sull'errore, chiamare [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror). **GetLastError** può restituire uno dei codici di errore seguenti.

<dl> <dt>

**ERRORE \_ buffer insufficiente \_**
</dt> <dt>

**flag di errore \_ non validi \_**
</dt> <dt>

**ERRORE \_ parametro non valido \_**
</dt> </dl>

## <a name="remarks"></a>Commenti

**GetDateFormatWrapW** offre la possibilità di utilizzare stringhe Unicode nei sistemi operativi precedenti a Windows XP. Il metodo preferito consiste nell'usare [**GetDateFormatW**](/windows/win32/api/datetimeapi/nf-datetimeapi-getdateformata) insieme a Microsoft Layer for Unicode (MSLU).

**GetDateFormatWrapW** deve essere chiamato direttamente da Shlwapi.dll, usando il numero ordinale 311.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional, \[ solo app desktop Windows XP\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shlwapi.dll (versione 5,0 o successiva)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**GetDateFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-getdateformata)
</dt> </dl>

 

 
