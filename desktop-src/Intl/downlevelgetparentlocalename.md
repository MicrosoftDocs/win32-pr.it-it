---
description: Recupera il nome delle impostazioni locali per l'elemento padre delle impostazioni locali fornite.
ms.assetid: a8db8107-822c-4bbc-acb8-40b25d2b41c4
title: Funzione DownlevelGetParentLocaleName (Nlsdl.h)
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
ms.openlocfilehash: af7580188c7ded31c80476509aef8a10ee83b1cb1f9767ca5819eed053f1ce87
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119898741"
---
# <a name="downlevelgetparentlocalename-function"></a>Funzione DownlevelGetParentLocaleName

Recupera il nome [delle impostazioni locali](locale-names.md) per l'elemento padre delle impostazioni locali fornite.

> [!Note]  
> Questa funzione viene usata solo dalle applicazioni eseguite in sistemi operativi Windows Vista. Per l'uso è necessario il pacchetto di download. Le applicazioni eseguite solo in Windows Vista e versioni successive devono chiamare [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) con *LCType* impostato su [LOCALE \_ SPARENT.](locale-sparent.md)

 

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

*Impostazioni locali* \[ Pollici\]
</dt> <dd>

[Identificatore delle impostazioni](locale-identifiers.md) locali delle impostazioni locali. È possibile utilizzare la macro [**MAKELCID**](/windows/desktop/api/Winnt/nf-winnt-makelcid) per creare un identificatore delle impostazioni locali o usare uno dei valori predefiniti seguenti.

-   [\_INVARIANTE DELLE IMPOSTAZIONI LOCALI](locale-invariant.md)
-   [IMPOSTAZIONI LOCALI \_ PREDEFINITE DEL \_ SISTEMA](locale-system-default.md)
-   [IMPOSTAZIONI LOCALI \_ PREDEFINITE \_ DELL'UTENTE](locale-user-default.md)

**Windows Vista e versioni successive:** Sono supportati anche gli identificatori delle impostazioni locali personalizzati seguenti.

-   [IMPOSTAZIONI LOCALI \_ PERSONALIZZATE \_ PREDEFINITE](locale-custom-constants.md)
-   [IMPOSTAZIONI LOCALI \_ PERSONALIZZATE \_ DELL'INTERFACCIA \_ UTENTE PREDEFINITE](locale-custom-constants.md)
-   [IMPOSTAZIONI \_ LOCALI PERSONALIZZATE NON \_ SPECIFICATE](locale-custom-constants.md)

</dd> <dt>

*lpName* \[ Cambio\]
</dt> <dd>

Puntatore a un buffer in cui la funzione recupera il nome delle impostazioni locali padre o uno dei valori predefiniti seguenti. Questo parametro è impostato su **NULL** se *cchName* è impostato su 0.

-   [\_INVARIANTE NOME \_ IMPOSTAZIONI LOCALI](locale-name-constants.md)
-   [IMPOSTAZIONI LOCALI \_ NAME \_ SYSTEM \_ DEFAULT](locale-name-constants.md)
-   [NOME IMPOSTAZIONI \_ LOCALI \_ PREDEFINITO \_ DELL'UTENTE](locale-name-constants.md)

</dd> <dt>

*cchName* \[ Pollici\]
</dt> <dd>

Dimensione del buffer indicata da *lpName*, in punti di codice UTF-16. Il valore 0 per questo parametro fa sì che la funzione ignori il buffer *lpName* e restituirà la dimensione del buffer, in caratteri (caratteri Null inclusi), necessaria per contenere il nome delle impostazioni locali padre.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il conteggio dei punti di codice UTF-16 nel nome delle impostazioni locali, incluso il carattere Null di terminazione, se l'operazione riesce.

Questa funzione restituisce 0 se non ha esito positivo. Per ottenere informazioni estese sull'errore, l'applicazione può [**chiamare GetLastError,**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)che può restituire uno dei codici di errore seguenti:

-   ERRORE \_ BUFFER \_ INSUFFICIENTE. Le dimensioni del buffer fornite non sono sufficienti o sono impostate in modo errato su **NULL.**
-   ERRORE \_ PARAMETRO NON \_ VALIDO. Uno dei valori dei parametri non è valido.

## <a name="remarks"></a>Commenti

Il file di intestazione e la DLL necessari fanno parte del download delle API di mapping dei dati di livello inferiore di Microsoft NLS, disponibile [nell'Area download Microsoft.](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&DisplayLang=en)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                           |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Componente ridistribuibile<br/>          | API di mapping dei dati di livello inferiore di Microsoft NLS in Windows XP con SP2 e versioni successive<br/>  |
| Intestazione<br/>                   | <dl> <dt>Nlsdl.h</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>NlsMap.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Supporto linguistico nazionale](national-language-support.md)
</dt> <dt>

[Funzioni di supporto per il linguaggio nazionale](national-language-support-functions.md)
</dt> <dt>

[Mapping dei dati delle impostazioni locali](mapping-locale-data.md)
</dt> <dt>

[**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa)
</dt> </dl>

 

 
