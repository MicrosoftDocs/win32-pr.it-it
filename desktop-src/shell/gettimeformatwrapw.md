---
description: Formatta l'ora come stringa temporale per le impostazioni locali specificate.
ms.assetid: 048b209c-f757-4b65-9ce7-282a5c21021f
title: GetTimeFormatWrapW (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetTimeFormatWrapW
api_type:
- DllExport
api_location:
- Shlwapi.dll
ms.openlocfilehash: 53f1bb88c2b3a79b58f3025daec31a7b1340b642
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979647"
---
# <a name="gettimeformatwrapw-function"></a>GetTimeFormatWrapW (funzione)

\[**GetTimeFormatWrapW** è disponibile per l'utilizzo in Windows XP. Potrebbe non essere disponibile nelle versioni successive. È consigliabile usare [**GetTimeFormatW**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata) al suo posto.\]

Formatta l'ora come stringa temporale per le impostazioni locali specificate. La funzione formatta un'ora specificata o l'ora di sistema locale.

> [!Note]  
> **GetTimeFormatWrapW** è un wrapper per la funzione **GetTimeFormatW** . Per ulteriori note sull'utilizzo, vedere la pagina [**GetTimeFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata) .

 

## <a name="syntax"></a>Sintassi


```C++
int GetTimeFormatWrapW(
  _In_        LCID       Locale,
  _In_        DWORD      dwFlags,
  _In_  const SYSTEMTIME *lpTime,
  _In_        LPCWSTR    pwzFormat,
  _Out_       LPWSTR     pwzTimeStr,
  _In_        int        cchTime
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Impostazioni locali* \[ in\]
</dt> <dd>

Tipo: **LCID**

Specifica le impostazioni locali per cui deve essere formattata la stringa dell'ora. Se *pwzFormat* è **null**, la funzione formatta la stringa in base al formato dell'ora per le impostazioni locali. Se *pwzFormat* non è **null**, la funzione usa le impostazioni locali solo per le informazioni non specificate nella stringa dell'immagine di formato (ad esempio, i marcatori temporali delle impostazioni locali).

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

Specifica varie opzioni di funzione. È possibile specificare una combinazione dei valori seguenti.

<dt>

<span id="LOCALE_NOUSEROVERRIDE"></span><span id="locale_nouseroverride"></span>

<span id="LOCALE_NOUSEROVERRIDE"></span><span id="locale_nouseroverride"></span>**impostazioni locali \_ NOUSEROVERRIDE**


</dt> <dd>

Se impostata, la funzione formatta la stringa utilizzando il formato di ora predefinito del sistema per le impostazioni locali specificate. Se non è impostato, la funzione formatta la stringa usando qualsiasi override utente nel formato di ora predefinito delle impostazioni locali. Questo flag può essere impostato solo se *pwzFormat* è **null**.

</dd> <dt>

<span id="LOCALE_USE_CP_ACP"></span><span id="locale_use_cp_acp"></span>

<span id="LOCALE_USE_CP_ACP"></span><span id="locale_use_cp_acp"></span>**impostazioni locali \_ usare \_ CP \_ ACP**


</dt> <dd>

Usa la tabella codici ANSI di sistema per la conversione di stringhe anziché la tabella codici delle impostazioni locali.

</dd> <dt>

<span id="TIME_NOMINUTESORSECONDS"></span><span id="time_nominutesorseconds"></span>

<span id="TIME_NOMINUTESORSECONDS"></span><span id="time_nominutesorseconds"></span>**TEMPO \_ NOMINUTESORSECONDS**


</dt> <dd>

Non usa minuti o secondi.

</dd> <dt>

<span id="TIME_NOSECONDS"></span><span id="time_noseconds"></span>

<span id="TIME_NOSECONDS"></span><span id="time_noseconds"></span>**TEMPO \_ NOsecondi**


</dt> <dd>

Non usa secondi.

</dd> <dt>

<span id="TIME_NOTIMEMARKER"></span><span id="time_notimemarker"></span>

<span id="TIME_NOTIMEMARKER"></span><span id="time_notimemarker"></span>**TEMPO \_ NOTIMEMARKER**


</dt> <dd>

Non utilizza un marcatore di ora.

</dd> <dt>

<span id="TIME_FORCE24HOURFORMAT"></span><span id="time_force24hourformat"></span>

<span id="TIME_FORCE24HOURFORMAT"></span><span id="time_force24hourformat"></span>**TEMPO \_ FORCE24HOURFORMAT**


</dt> <dd>

Usa sempre il formato a 24 ore.

</dd> </dl> </dd> <dt>

*lpTime* \[ in\]
</dt> <dd>

Tipo: **const [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) \** _

Puntatore a una struttura [_ *SYSTEMTIME* *](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) che contiene le informazioni sull'ora da formattare. Se questo puntatore è **null**, la funzione usa l'ora di sistema locale corrente.

</dd> <dt>

*pwzFormat* \[ in\]
</dt> <dd>

Tipo: **LPCWSTR**

Puntatore a un formato da utilizzare per formare la stringa dell'ora. Se *pwzFormat* è **null**, la funzione userà il formato dell'ora delle impostazioni locali specificate. Per ulteriori informazioni, vedere [**GetTimeFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata) .

</dd> <dt>

*pwzTimeStr* \[ out\]
</dt> <dd>

Tipo: **LPWSTR**

Puntatore a un buffer che riceve la stringa di tempo formattata.

</dd> <dt>

*cchTime* \[ in\]
</dt> <dd>

Tipo: **int**

Dimensione, in caratteri, del buffer *pwzTimeStr* . Se *cchTime* è zero, la funzione restituisce il numero di caratteri necessari per memorizzare la stringa di tempo formattata e il buffer a cui punta *pwzTimeStr* non viene utilizzato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **int**

Se la funzione ha esito positivo, il valore restituito è il numero di caratteri scritti nel buffer a cui punta *pwzTimeStr*. Se il parametro *cchTime* è zero, il valore restituito è il numero di caratteri necessari per conservare la stringa di tempo formattata. Il conteggio include il carattere null di terminazione.

Se la funzione ha esito negativo, il valore restituito è zero. Per informazioni dettagliate sull'errore, chiamare [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror). **GetLastError** può restituire uno dei codici di errore seguenti.

<dl> <dt>

**ERRORE \_ buffer insufficiente \_**
</dt> <dt>

**flag di errore \_ non validi \_**
</dt> <dt>

**ERRORE \_ parametro non valido \_**
</dt> </dl>

## <a name="remarks"></a>Commenti

**GetTimeFormatWrapW** offre la possibilità di utilizzare stringhe Unicode nei sistemi operativi precedenti a Windows XP. Il metodo preferito consiste nell'usare [**GetTimeFormatW**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata) insieme a Microsoft Layer for Unicode (MSLU).

**GetTimeFormatWrapW** deve essere chiamato direttamente da Shlwapi.dll, usando il numero ordinale 310.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional, \[ solo app desktop Windows XP\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shlwapi.dll (versione 5,0 o successiva)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**GetTimeFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata)
</dt> </dl>

 

 
