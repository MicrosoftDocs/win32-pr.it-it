---
description: Confronta due stringhe di caratteri Unicode, usando le impostazioni locali specificate.
ms.assetid: dff16c1b-d329-40de-b8d7-91edb36ce198
title: CompareStringWrapW (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CompareStringWrapW
api_type:
- DllExport
api_location:
- Shlwapi.dll
ms.openlocfilehash: 0731182f5c01ad56db722972628d2cbe39373835
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977383"
---
# <a name="comparestringwrapw-function"></a>CompareStringWrapW (funzione)

\[**CompareStringWrapW** è disponibile per l'utilizzo in Windows XP. Non sarà disponibile nelle versioni successive. È consigliabile usare [**CompareStringW**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) al suo posto.\]

Confronta due stringhe di caratteri Unicode, usando le impostazioni locali specificate.

> [!Note]  
> **CompareStringWrapW** è un wrapper per la funzione **CompareStringW** . Per ulteriori note sull'utilizzo, vedere la pagina [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) .

 

## <a name="syntax"></a>Sintassi


```C++
int CompareStringWrapW(
  _In_ LCID    Locale,
  _In_ DWORD   dwCmpFlags,
  _In_ LPCWSTR lpString1,
  _In_ int     cchCount1,
  _In_ LPCWSTR lpString2,
  _In_ int     cchCount2
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Impostazioni locali* \[ in\]
</dt> <dd>

Tipo: **LCID**

Identificatore delle impostazioni locali utilizzato per il confronto. Questo parametro può essere uno dei seguenti identificatori delle impostazioni locali predefiniti o un identificatore delle impostazioni locali creato dalla macro [**MAKELCID**](/windows/win32/api/winnt/nf-winnt-makelcid) .

<dt>

<span id="LOCALE_SYSTEM_DEFAULT"></span><span id="locale_system_default"></span>

<span id="LOCALE_SYSTEM_DEFAULT"></span><span id="locale_system_default"></span>**impostazioni locali del \_ sistema \_**


</dt> <dd>

Impostazioni locali predefinite del sistema.

</dd> <dt>

<span id="LOCALE_USER_DEFAULT"></span><span id="locale_user_default"></span>

<span id="LOCALE_USER_DEFAULT"></span><span id="locale_user_default"></span>**\_impostazione predefinita utente impostazioni locali \_**


</dt> <dd>

Impostazioni locali predefinite dell'utente corrente.

</dd> </dl> </dd> <dt>

*dwCmpFlags* \[ in\]
</dt> <dd>

Tipo: **DWORD**

Flag che indicano il modo in cui la funzione Confronta le due stringhe. Per impostazione predefinita, questi flag non sono impostati. Impostare su zero per ottenere il comportamento predefinito o per qualsiasi combinazione dei valori seguenti.

<dt>

<span id="NORM_IGNORECASE"></span><span id="norm_ignorecase"></span>

<span id="NORM_IGNORECASE"></span><span id="norm_ignorecase"></span>**\_IgnoreCase Norm**


</dt> <dd>

Ignora maiuscole/minuscole.

</dd> <dt>

<span id="NORM_IGNOREKANATYPE"></span><span id="norm_ignorekanatype"></span>

<span id="NORM_IGNOREKANATYPE"></span><span id="norm_ignorekanatype"></span>**\_IGNOREKANATYPE Norm**


</dt> <dd>

Non distinguere tra caratteri Hiragana e katakana. I caratteri Hiragana e Katakana corrispondenti vengono considerati uguali.

</dd> <dt>

<span id="NORM_IGNORENONSPACE"></span><span id="norm_ignorenonspace"></span>

<span id="NORM_IGNORENONSPACE"></span><span id="norm_ignorenonspace"></span>**\_IGNORENONSPACE Norm**


</dt> <dd>

Ignora caratteri senza spaziatura.

</dd> <dt>

<span id="NORM_IGNORESYMBOLS"></span><span id="norm_ignoresymbols"></span>

<span id="NORM_IGNORESYMBOLS"></span><span id="norm_ignoresymbols"></span>**\_IGNORESYMBOLS Norm**


</dt> <dd>

Ignorare i simboli.

</dd> <dt>

<span id="NORM_IGNOREWIDTH"></span><span id="norm_ignorewidth"></span>

<span id="NORM_IGNOREWIDTH"></span><span id="norm_ignorewidth"></span>**\_IGNOREWIDTH Norm**


</dt> <dd>

Non distinguere tra un carattere a byte singolo e lo stesso carattere di un carattere a byte doppio.

</dd> <dt>

<span id="SORT_STRINGSORT"></span><span id="sort_stringsort"></span>

<span id="SORT_STRINGSORT"></span><span id="sort_stringsort"></span>**Ordina \_ STRINGSORT**


</dt> <dd>

Considera la punteggiatura uguale ai simboli.

</dd> </dl> </dd> <dt>

*lpString1* \[ in\]
</dt> <dd>

Tipo: **LPCWSTR**

Puntatore alla prima stringa Unicode da confrontare.

</dd> <dt>

*cchCount1* \[ in\]
</dt> <dd>

Tipo: **int**

Numero di caratteri nella stringa a cui punta il parametro *lpString1* . Il conteggio non include il carattere null di terminazione. Se questo parametro è un valore negativo, si presuppone che la stringa sia con terminazione null e che la lunghezza venga calcolata automaticamente.

</dd> <dt>

*lpString2* \[ in\]
</dt> <dd>

Tipo: **LPCWSTR**

Puntatore alla seconda stringa Unicode da confrontare.

</dd> <dt>

*cchCount2* \[ in\]
</dt> <dd>

Tipo: **int**

Numero di caratteri nella stringa a cui punta il parametro *lpString2* . Il conteggio non include il carattere null di terminazione. Se questo parametro è un valore negativo, si presuppone che la stringa sia con terminazione null e che la lunghezza venga calcolata automaticamente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **int**

Se la funzione ha esito negativo, il valore restituito è zero. Per informazioni dettagliate sull'errore, chiamare [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror). **GetLastError** può restituire uno dei codici di errore seguenti.

-   flag di errore \_ non validi \_
-   ERRORE \_ parametro non valido \_

Se la funzione ha esito positivo, il valore restituito è uno dei valori seguenti. 

| Requisito | Valore |
|---------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| CSTR \_ minore \_ di    | La stringa a cui punta il parametro *lpString1* è minore del valore lessicale rispetto alla stringa a cui punta il parametro *lpString2* . |
| CSTR \_ uguale a         | La stringa a cui punta *lpString1* è uguale al valore lessicale alla stringa a cui punta *lpString2*.                              |
| CSTR \_ maggiore \_ di | La stringa a cui punta *lpString1* è maggiore nel valore lessicale della stringa a cui punta *lpString2*                           |



 

## <a name="remarks"></a>Commenti

**Avviso di sicurezza:** L'uso errato di questa funzione può compromettere la sicurezza dell'applicazione. Le stringhe che non vengono confrontate correttamente possono produrre un input non valido. Testare le stringhe per assicurarsi che siano valide prima di utilizzarle e fornire gestori di errori. Per altre informazioni, vedere [considerazioni sulla sicurezza: funzionalità internazionali](../intl/security-considerations--international-features.md)

Il metodo preferito consiste nell'usare [**CompareStringW**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) insieme a Microsoft Layer for Unicode (MSLU).

**CompareStringWrapW** deve essere chiamato direttamente da Shlwapi.dll, usando il numero ordinale 45.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional, \[ solo app desktop Windows XP\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Nessuno</dt> </dl>                               |
| DLL<br/>                      | <dl> <dt>Shlwapi.dll (versione 5,0 o successiva)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw)
</dt> </dl>

 

 
