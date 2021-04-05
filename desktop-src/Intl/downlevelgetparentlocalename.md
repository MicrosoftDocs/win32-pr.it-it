---
description: Recupera il nome delle impostazioni locali per l'elemento padre delle impostazioni locali specificate.
ms.assetid: a8db8107-822c-4bbc-acb8-40b25d2b41c4
title: Funzione DownlevelGetParentLocaleName (nlsdl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DownlevelGetParentLocaleName
api_type:
- DllExport
api_location:
- NlsMap.dll
ms.openlocfilehash: d3a556d68c33249d2e6b49c48035cc58d8bac8e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968320"
---
# <a name="downlevelgetparentlocalename-function"></a>DownlevelGetParentLocaleName (funzione)

Recupera il [nome delle impostazioni locali](locale-names.md) per l'elemento padre delle impostazioni locali specificate.

> [!Note]  
> Questa funzione viene utilizzata solo dalle applicazioni eseguite in sistemi operativi precedenti a Windows Vista. Il relativo utilizzo richiede il pacchetto di download. Le applicazioni che vengono eseguite solo in Windows Vista e versioni successive devono chiamare [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) con *LCType* impostato su [locale \_ SPARENT](locale-sparent.md).

 

## <a name="syntax"></a>Sintassi


```C++
int DownlevelGetParentLocaleName(
  _In_  LCID   Locale,
  _Out_ LPWSTR lpName,
  _In_  int    cchName
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Impostazioni locali* \[ in\]
</dt> <dd>

[Identificatore](locale-identifiers.md) delle impostazioni locali delle impostazioni locali. È possibile usare la macro [**MAKELCID**](/windows/desktop/api/Winnt/nf-winnt-makelcid) per creare un identificatore delle impostazioni locali o usare uno dei valori predefiniti seguenti.

-   [impostazioni locali \_ INvariabili](locale-invariant.md)
-   [impostazioni locali del \_ sistema \_](locale-system-default.md)
-   [\_impostazione predefinita utente impostazioni locali \_](locale-user-default.md)

**Windows Vista e versioni successive:** Sono supportati anche gli identificatori delle impostazioni locali personalizzati seguenti.

-   [impostazioni locali \_ personalizzate \_ predefinite](locale-custom-constants.md)
-   [\_ \_ impostazione predefinita interfaccia utente personalizzata impostazioni locali \_](locale-custom-constants.md)
-   [impostazioni locali \_ personalizzate non \_ specificate](locale-custom-constants.md)

</dd> <dt>

*lpName* \[ out\]
</dt> <dd>

Puntatore a un buffer in cui la funzione recupera il nome delle impostazioni locali padre o uno dei seguenti valori predefiniti. Questo parametro è impostato su **null** se *cchName* è impostato su 0.

-   [nome delle impostazioni locali \_ \_ invariante](locale-name-constants.md)
-   [impostazioni locali \_ nome \_ sistema \_ predefinito](locale-name-constants.md)
-   [\_ \_ impostazione predefinita utente nome impostazioni locali \_](locale-name-constants.md)

</dd> <dt>

*cchName* \[ in\]
</dt> <dd>

Dimensioni del buffer indicato da *lpName*, in punti di codice UTF-16. Il valore 0 per questo parametro fa in modo che la funzione ignori il buffer *lpName* e restituisca la dimensione del buffer, in caratteri (caratteri null inclusi), necessaria per contenere il nome delle impostazioni locali padre.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il numero di punti di codice UTF-16 nel nome delle impostazioni locali, incluso il carattere null di terminazione, in caso di esito positivo.

Questa funzione restituisce 0 in caso di esito negativo. Per ottenere informazioni estese sull'errore, l'applicazione può chiamare [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), che può restituire uno dei codici di errore seguenti:

-   ERRORE \_ \_ nel buffer insufficiente. Una dimensione del buffer specificata non è sufficientemente grande oppure è stata impostata erroneamente su **null**.
-   ERRORE \_ parametro non valido \_ . Uno dei valori di parametro non è valido.

## <a name="remarks"></a>Commenti

Il file di intestazione e la DLL necessari fanno parte del download di "Microsoft NLS Data Mapping API", disponibile nell' [area download Microsoft](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&DisplayLang=en).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Componente ridistribuibile<br/>          | API di mapping dei dati di livello inferiore Microsoft NLS in Windows XP con SP2 e versioni successive<br/>  |
| Intestazione<br/>                   | <dl> <dt>Nlsdl. h</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>NlsMap.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Supporto per lingua nazionale](national-language-support.md)
</dt> <dt>

[Funzioni di supporto del linguaggio nazionale](national-language-support-functions.md)
</dt> <dt>

[Mapping dei dati delle impostazioni locali](mapping-locale-data.md)
</dt> <dt>

[**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa)
</dt> </dl>

 

 
