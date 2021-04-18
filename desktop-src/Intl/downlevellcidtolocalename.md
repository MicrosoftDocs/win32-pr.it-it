---
description: Converte un identificatore delle impostazioni locali in un nome delle impostazioni locali.
ms.assetid: 8e40d097-08a2-43e8-88e8-a4ecaddf449a
title: Funzione DownlevelLCIDToLocaleName (nlsdl. h)
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
ms.openlocfilehash: 2f8e4ce9763348cf765522ebbd624a6e82f1071a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317162"
---
# <a name="downlevellcidtolocalename-function"></a>DownlevelLCIDToLocaleName (funzione)

Converte un [identificatore delle impostazioni locali](locale-identifiers.md) in un [nome delle impostazioni locali](locale-names.md).

> [!Note]  
> Questa funzione viene utilizzata solo dalle applicazioni eseguite in sistemi operativi precedenti a Windows Vista. Il relativo utilizzo richiede un pacchetto di download. Le applicazioni che vengono eseguite solo in Windows Vista e versioni successive devono chiamare [**LCIDToLocaleName**](/windows/desktop/api/Winnls/nf-winnls-lcidtolocalename) per recuperare un nome delle impostazioni locali.

 

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

*Impostazioni locali* \[ in\]
</dt> <dd>

Identificatore delle impostazioni locali da tradurre. È possibile usare la macro [**MAKELCID**](/windows/desktop/api/Winnt/nf-winnt-makelcid) per creare un identificatore delle impostazioni locali. Questa funzione non supporta le impostazioni locali non associate ad alcun paese o i seguenti valori specifici dell'identificatore delle impostazioni locali.

-   [impostazioni locali del \_ sistema \_](locale-system-default.md)
-   [\_impostazione predefinita utente impostazioni locali \_](locale-user-default.md)
-   [impostazioni locali \_ personalizzate \_ predefinite](locale-custom-constants.md)
-   [\_ \_ impostazione predefinita interfaccia utente personalizzata impostazioni locali \_](locale-custom-constants.md)
-   [impostazioni locali \_ personalizzate non \_ specificate](locale-custom-constants.md)

</dd> <dt>

*lpName* \[ out\]
</dt> <dd>

Puntatore a un buffer in cui questa funzione recupera il nome delle impostazioni locali. La funzione recupera **null** se *cchName* è impostato su 0.

</dd> <dt>

*cchName* \[ in\]
</dt> <dd>

Dimensioni, in punti di codice UTF-16, del buffer del nome delle impostazioni locali. L'applicazione imposta questo parametro su 0 per restituire la dimensione richiesta del buffer del nome delle impostazioni locali.

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Flag che specificano il tipo di nome da recuperare. Il valore predefinito è il \_ nome delle impostazioni locali di livello inferiore \_ .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il numero di punti di codice UTF-16 nel nome delle impostazioni locali, incluso il carattere null di terminazione, in caso di esito positivo. Se la funzione ha esito positivo e il valore di *cchName* è 0, il valore restituito è la dimensione richiesta, in caratteri (compresi i caratteri null), per il buffer del nome delle impostazioni locali.

Se l'operazione non riesce, la funzione restituisce 0. Per ottenere informazioni estese sull'errore, l'applicazione può chiamare [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), che può restituire uno dei codici di errore seguenti:

-   ERRORE \_ \_ nel buffer insufficiente. Una dimensione del buffer specificata non è sufficientemente grande oppure è stata impostata erroneamente su **null**.
-   flag di errore \_ non validi \_ . Il valore di *dwFlags* non è valido.
-   ERRORE \_ parametro non valido \_ . Uno dei valori di parametro non è valido.

## <a name="remarks"></a>Commenti

> [!Note]  
> Questa funzione non supporta [impostazioni locali personalizzate](custom-locales.md).

 

Il file di intestazione e la DLL necessari fanno parte del download di "Microsoft NLS Data Mapping API", disponibile nell' [area download Microsoft](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&DisplayLang=en).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                                         |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                |
| Componente ridistribuibile<br/>          | API di mapping dei dati di livello inferiore Microsoft NLS in Windows XP con SP2 e laterorWindows vista<br/> |
| Intestazione<br/>                   | <dl> <dt>Nlsdl. h</dt> </dl>                  |
| DLL<br/>                      | <dl> <dt>NlsMap.dll</dt> </dl>               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Supporto per lingua nazionale](national-language-support.md)
</dt> <dt>

[Funzioni di supporto del linguaggio nazionale](national-language-support-functions.md)
</dt> <dt>

[Mapping dei dati delle impostazioni locali](mapping-locale-data.md)
</dt> <dt>

[**LCIDToLocaleName**](/windows/desktop/api/Winnls/nf-winnls-lcidtolocalename)
</dt> </dl>

 

 
