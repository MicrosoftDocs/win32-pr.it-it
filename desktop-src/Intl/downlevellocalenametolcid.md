---
description: Converte un nome delle impostazioni locali in un identificatore delle impostazioni locali che può essere usato per ottenere informazioni dal sistema operativo.
ms.assetid: dc776c41-0376-4222-bebf-86be7e4be122
title: Funzione DownlevelLocaleNameToLCID (Nlsdl.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DownlevelLocaleNameToLCID
api_type:
- DllExport
api_location:
- NlsMap.dll
ms.openlocfilehash: 39a0a6b274ba141553d2ddda927f71754cc9639ff5fc3a0d3870a974e46526a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119898731"
---
# <a name="downlevellocalenametolcid-function"></a>Funzione DownlevelLocaleNameToLCID

Converte un [nome delle impostazioni](locale-names.md) locali in un identificatore delle impostazioni locali che può essere usato per ottenere informazioni dal sistema operativo. [](locale-identifiers.md)

> [!Note]  
> Questa funzione viene usata solo dalle applicazioni eseguite in sistemi operativi Windows Vista. Il suo uso richiede un pacchetto di download. Le applicazioni eseguite solo in Windows Vista e versioni successive devono chiamare [**LocaleNameToLCID**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid) per recuperare un identificatore delle impostazioni locali.

 

## <a name="syntax"></a>Sintassi


```C++
LCID DownlevelLocaleNameToLCID(
  _In_ LPWSTR lpName,
  _In_ DWORD  dwFlags
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lpName* \[ Pollici\]
</dt> <dd>

Puntatore a una stringa con terminazione Null che rappresenta un [nome di impostazioni locali](locale-names.md).

</dd> <dt>

*dwFlags* \[ Pollici\]
</dt> <dd>

Flag che specificano il tipo di nome. Il valore predefinito è DOWNLEVEL \_ LOCALE \_ NAME.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'identificatore delle impostazioni locali che corrisponde al nome delle impostazioni locali in caso di esito positivo.

La funzione restituisce 0 se non ha esito positivo. Per ottenere informazioni estese sugli errori, l'applicazione può chiamare [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), che può restituire uno dei codici di errore seguenti:

-   ERRORE \_ FLAG NON \_ VALIDI. I valori forniti per i flag non sono validi.
-   ERRORE \_ PARAMETRO \_ NON VALIDO. Uno dei valori dei parametri non è valido.

## <a name="remarks"></a>Commenti

> [!Note]  
> Questa funzione non supporta le impostazioni locali neutre. La funzione [**LocaleNameToLCID**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid) equivalente supporta le impostazioni locali [personalizzate,](custom-locales.md)ma solo per Windows Vista e versioni successive.

 

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

[**LocaleNameToLCID**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid)
</dt> </dl>

 

 
