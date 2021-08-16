---
description: Confronta due stringhe di caratteri Unicode, usando le impostazioni locali specificate.
ms.assetid: dff16c1b-d329-40de-b8d7-91edb36ce198
title: Funzione CompareStringWrapW
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
ms.openlocfilehash: 9fe05c354aaa901d87c77ba04eecd5dc4efd925d77bdeaf5387a137d85b27348
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117861512"
---
# <a name="comparestringwrapw-function"></a>Funzione CompareStringWrapW

\[**CompareStringWrapW** è disponibile per l'uso in Windows XP. Non sarà disponibile nelle versioni successive. È [**consigliabile usare CompareStringW**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) al suo posto.\]

Confronta due stringhe di caratteri Unicode, usando le impostazioni locali specificate.

> [!Note]  
> **CompareStringWrapW** è un wrapper per la **funzione CompareStringW.** Per altre note sull'utilizzo, vedere la pagina [**CompareString.**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw)

 

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

*Impostazioni locali* \[ Pollici\]
</dt> <dd>

Tipo: **LCID**

Identificatore delle impostazioni locali utilizzato per il confronto. Questo parametro può essere uno degli identificatori delle impostazioni locali predefiniti seguenti o un identificatore delle impostazioni locali creato dalla macro [**MAKELCID.**](/windows/win32/api/winnt/nf-winnt-makelcid)

<dt>

<span id="LOCALE_SYSTEM_DEFAULT"></span><span id="locale_system_default"></span>

<span id="LOCALE_SYSTEM_DEFAULT"></span><span id="locale_system_default"></span>**IMPOSTAZIONI LOCALI \_ PREDEFINITE DEL \_ SISTEMA**


</dt> <dd>

Impostazioni locali predefinite del sistema.

</dd> <dt>

<span id="LOCALE_USER_DEFAULT"></span><span id="locale_user_default"></span>

<span id="LOCALE_USER_DEFAULT"></span><span id="locale_user_default"></span>**IMPOSTAZIONI LOCALI \_ PREDEFINITE \_ DELL'UTENTE**


</dt> <dd>

Impostazioni locali predefinite dell'utente corrente.

</dd> </dl> </dd> <dt>

*dwCmpFlags* \[ Pollici\]
</dt> <dd>

Tipo: **DWORD**

Flag che indicano il modo in cui la funzione confronta le due stringhe. Per impostazione predefinita, questi flag non sono impostati. Impostare su zero per ottenere il comportamento predefinito o su qualsiasi combinazione dei valori seguenti.

<dt>

<span id="NORM_IGNORECASE"></span><span id="norm_ignorecase"></span>

<span id="NORM_IGNORECASE"></span><span id="norm_ignorecase"></span>**NORM \_ IGNORECASE**


</dt> <dd>

Ignorare la distinzione tra maiuscole e minuscole.

</dd> <dt>

<span id="NORM_IGNOREKANATYPE"></span><span id="norm_ignorekanatype"></span>

<span id="NORM_IGNOREKANATYPE"></span><span id="norm_ignorekanatype"></span>**NORM \_ IGNOREKANATYPE**


</dt> <dd>

Non distinguere tra caratteri Hiragana e Katakana. I caratteri Hiragana e Katakana corrispondenti vengono confrontati come uguali.

</dd> <dt>

<span id="NORM_IGNORENONSPACE"></span><span id="norm_ignorenonspace"></span>

<span id="NORM_IGNORENONSPACE"></span><span id="norm_ignorenonspace"></span>**NORM \_ IGNORENONSPACE**


</dt> <dd>

Ignorare i caratteri nonspacing.

</dd> <dt>

<span id="NORM_IGNORESYMBOLS"></span><span id="norm_ignoresymbols"></span>

<span id="NORM_IGNORESYMBOLS"></span><span id="norm_ignoresymbols"></span>**NORM \_ IGNORESYMBOLS**


</dt> <dd>

Ignorare i simboli.

</dd> <dt>

<span id="NORM_IGNOREWIDTH"></span><span id="norm_ignorewidth"></span>

<span id="NORM_IGNOREWIDTH"></span><span id="norm_ignorewidth"></span>**NORM \_ IGNOREWIDTH**


</dt> <dd>

Non distinguere tra un carattere a byte singolo e lo stesso carattere di un carattere a byte doppio.

</dd> <dt>

<span id="SORT_STRINGSORT"></span><span id="sort_stringsort"></span>

<span id="SORT_STRINGSORT"></span><span id="sort_stringsort"></span>**ORDINAMENTO \_ DI STRINGHESORT**


</dt> <dd>

La punteggiatura viene trattata come simboli.

</dd> </dl> </dd> <dt>

*lpString1* \[ Pollici\]
</dt> <dd>

Tipo: **LPCWSTR**

Puntatore alla prima stringa Unicode da confrontare.

</dd> <dt>

*cchCount1* \[ Pollici\]
</dt> <dd>

Tipo: **int**

Numero di caratteri nella stringa a cui punta il *parametro lpString1.* Il conteggio non include il carattere Null di terminazione. Se questo parametro è un valore negativo, si presuppone che la stringa sia con terminazione Null e che la lunghezza venga calcolata automaticamente.

</dd> <dt>

*lpString2* \[ Pollici\]
</dt> <dd>

Tipo: **LPCWSTR**

Puntatore alla seconda stringa Unicode da confrontare.

</dd> <dt>

*cchCount2* \[ Pollici\]
</dt> <dd>

Tipo: **int**

Numero di caratteri nella stringa a cui punta il *parametro lpString2.* Il conteggio non include il carattere Null di terminazione. Se questo parametro è un valore negativo, si presuppone che la stringa sia con terminazione Null e che la lunghezza venga calcolata automaticamente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **int**

Se la funzione ha esito negativo, il valore restituito è zero. Per informazioni dettagliate sull'errore, chiamare [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror). **GetLastError può** restituire uno dei codici di errore seguenti.

-   FLAG \_ DI ERRORE NON \_ VALIDI
-   ERRORE \_ PARAMETRO NON \_ VALIDO

Se la funzione ha esito positivo, il valore restituito è uno dei valori seguenti. 

| Requisito | Valore |
|---------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| CSTR \_ MINORE \_ DI    | La stringa a cui punta *il parametro lpString1* è minore nel valore lessicale rispetto alla stringa a cui punta *il parametro lpString2.* |
| CSTR \_ UGUALE         | La stringa a cui punta *lpString1* è uguale nel valore lessicale alla stringa a cui *punta lpString2*.                              |
| CSTR \_ MAGGIORE \_ DI | La stringa a cui punta *lpString1* è maggiore nel valore lessicale rispetto alla stringa a cui punta *lpString2*                           |



 

## <a name="remarks"></a>Commenti

**Avviso di sicurezza:** L'uso non corretto di questa funzione può compromettere la sicurezza dell'applicazione. Le stringhe che non vengono confrontate correttamente possono produrre input non valido. Testare le stringhe per assicurarsi che siano valide prima di usarle e fornire gestori degli errori. Per altre informazioni, vedere [Considerazioni sulla sicurezza: funzionalità internazionali](../intl/security-considerations--international-features.md)

Il metodo preferito è usare [**CompareStringW**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) insieme al livello Microsoft per Unicode (MSLU).

**CompareStringWrapW** deve essere chiamato direttamente da Shlwapi.dll, usando il numero ordinale 45.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional, Windows solo app desktop XP \[\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Nessuno</dt> </dl>                               |
| DLL<br/>                      | <dl> <dt>Shlwapi.dll (versione 5.0 o successiva)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw)
</dt> </dl>

 

 
