---
description: Converte un identificatore delle impostazioni locali in un nome di impostazioni locali.
ms.assetid: 8e40d097-08a2-43e8-88e8-a4ecaddf449a
title: Funzione DownlevelLCIDToLocaleName (Nlsdl.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DownlevelLCIDToLocaleName
api_type:
- DllExport
api_location:
- NlsMap.dll
ms.openlocfilehash: b96d0c983c46c5d16007aae3a59659099a48855048194153d0c8102d26dc5bd2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119898721"
---
# <a name="downlevellcidtolocalename-function"></a>Funzione DownlevelLCIDToLocaleName

Converte un identificatore [delle impostazioni locali](locale-identifiers.md) in un nome di impostazioni [locali](locale-names.md).

> [!Note]  
> Questa funzione viene usata solo dalle applicazioni eseguite in sistemi operativi Windows Vista. Il suo uso richiede un pacchetto di download. Le applicazioni eseguite solo in Windows Vista e versioni successive devono chiamare [**LCIDToLocaleName**](/windows/desktop/api/Winnls/nf-winnls-lcidtolocalename) per recuperare un nome delle impostazioni locali.

 

## <a name="syntax"></a>Sintassi


```C++
int DownlevelLCIDToLocaleName(
  _In_  LCID   Locale,
  _Out_ LPWSTR lpName,
  _In_  int    cchName,
  _In_  DWORD  dwFlags
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Impostazioni locali* \[ Pollici\]
</dt> <dd>

Identificatore delle impostazioni locali da convertire. È possibile usare la macro [**MAKELCID**](/windows/desktop/api/Winnt/nf-winnt-makelcid) per creare un identificatore delle impostazioni locali. Questa funzione non supporta le impostazioni locali neutre o i valori dell'identificatore delle impostazioni locali specifici seguenti.

-   [IMPOSTAZIONI LOCALI \_ PREDEFINITE DEL \_ SISTEMA](locale-system-default.md)
-   [IMPOSTAZIONI LOCALI \_ PREDEFINITE \_ DELL'UTENTE](locale-user-default.md)
-   [IMPOSTAZIONI \_ LOCALI PERSONALIZZATE \_ PREDEFINITE](locale-custom-constants.md)
-   [IMPOSTAZIONE PREDEFINITA \_ \_ DELL'INTERFACCIA \_ UTENTE PERSONALIZZATA DELLE IMPOSTAZIONI LOCALI](locale-custom-constants.md)
-   [IMPOSTAZIONI \_ LOCALI PERSONALIZZATE NON \_ SPECIFICATE](locale-custom-constants.md)

</dd> <dt>

*lpName* \[ Cambio\]
</dt> <dd>

Puntatore a un buffer in cui questa funzione recupera il nome delle impostazioni locali. La funzione recupera **NULL se** *cchName* è impostato su 0.

</dd> <dt>

*cchName* \[ Pollici\]
</dt> <dd>

Dimensione, in punti di codice UTF-16, del buffer dei nomi delle impostazioni locali. L'applicazione imposta questo parametro su 0 per restituire le dimensioni richieste del buffer dei nomi delle impostazioni locali.

</dd> <dt>

*dwFlags* \[ Pollici\]
</dt> <dd>

Flag che specificano il tipo di nome da recuperare. Il valore predefinito è DOWNLEVEL \_ LOCALE \_ NAME.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il conteggio dei punti di codice UTF-16 nel nome delle impostazioni locali, incluso il carattere Null di terminazione, in caso di esito positivo. Se la funzione ha esito positivo e il valore di *cchName* è 0, il valore restituito è la dimensione richiesta, in caratteri (inclusi i caratteri Null), per il buffer dei nomi delle impostazioni locali.

La funzione restituisce 0 se non ha esito positivo. Per ottenere informazioni estese sull'errore, l'applicazione può chiamare [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), che può restituire uno dei codici di errore seguenti:

-   ERRORE \_ BUFFER \_ INSUFFICIENTE. Le dimensioni del buffer specificate non erano sufficienti o non erano impostate in modo errato su **NULL.**
-   ERRORE \_ FLAG NON \_ VALIDI. Il valore *di dwFlags* non è valido.
-   ERRORE \_ PARAMETRO \_ NON VALIDO. I valori dei parametri non sono validi.

## <a name="remarks"></a>Commenti

> [!Note]  
> Questa funzione non supporta le [impostazioni locali personalizzate.](custom-locales.md)

 

Il file di intestazione e la DLL necessari fanno parte del download "Microsoft NLS Downlevel Data Mapping APIs", disponibile [nell'Area download Microsoft.](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&DisplayLang=en)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                                         |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                                |
| Componente ridistribuibile<br/>          | API di mapping dei dati di livello inferiore di Microsoft NLS in Windows XP con SP2 e versioni successiveWindows Vista<br/> |
| Intestazione<br/>                   | <dl> <dt>Nlsdl.h</dt> </dl>                  |
| DLL<br/>                      | <dl> <dt>NlsMap.dll</dt> </dl>               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Supporto linguistico nazionale](national-language-support.md)
</dt> <dt>

[Funzioni di supporto linguistico nazionale](national-language-support-functions.md)
</dt> <dt>

[Mapping dei dati delle impostazioni locali](mapping-locale-data.md)
</dt> <dt>

[**LCIDToLocaleName**](/windows/desktop/api/Winnls/nf-winnls-lcidtolocalename)
</dt> </dl>

 

 
