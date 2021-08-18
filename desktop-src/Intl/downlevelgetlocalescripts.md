---
description: Fornisce un elenco di script per le impostazioni locali specificate.
ms.assetid: 0cedcf6c-bab4-4e0f-ab8f-04aa8e51602f
title: Funzione DownlevelGetLocaleScripts (Idndl.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DownlevelGetLocaleScripts
api_type:
- DllExport
api_location:
- Idndl.dll
ms.openlocfilehash: 02631a605f67f3c27dfcc29c1e660ca24e56b6072d4490ba8ba090ebdd8b9019
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119068251"
---
# <a name="downlevelgetlocalescripts-function"></a>Funzione DownlevelGetLocaleScripts

Fornisce un elenco di script per le impostazioni locali specificate.

> [!Note]  
> Questa funzione viene usata solo dalle applicazioni eseguite in sistemi operativi Windows Vista. L'uso richiede il pacchetto di download. Le applicazioni eseguite solo in Windows Vista e versioni successive devono chiamare [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) con *LCType* impostato su [LOCALE \_ SSCRIPTS](locale-sscripts.md).

 

## <a name="syntax"></a>Sintassi


```C++
int DownlevelGetLocaleScripts(
  _In_  LPCWSTR lpLocaleName,
  _Out_ LPWSTR  lpScripts,
  _In_  int     cchScripts
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lpLocaleName* \[ Pollici\]
</dt> <dd>

Puntatore a un nome delle impostazioni locali con [terminazione Null.](locale-names.md)

</dd> <dt>

*lpScripts* \[ Cambio\]
</dt> <dd>

Puntatore a un buffer in cui questa funzione recupera una stringa con terminazione Null che rappresenta un elenco di script, usando la notazione a 4 caratteri usata in [ISO 15924.](https://www.unicode.org/iso15924/iso15924-codes.html) Ogni nome di script è costituito da quattro caratteri latini e i nomi vengono recuperati in ordine alfabetico. Ognuno di essi, incluso l'ultimo, è seguito da un punto e virgola.

In alternativa, questo parametro può **contenere NULL** se *cchScripts* è impostato su 0. In questo caso, la funzione restituisce le dimensioni richieste per il buffer di script.

</dd> <dt>

*cchScripts* \[ Pollici\]
</dt> <dd>

Dimensione, in caratteri, per il buffer di script indicato da *lpScripts*.

In alternativa, l'applicazione può impostare questo parametro su 0. In questo caso, la funzione recupera **NULL** in *lpScripts* e restituisce le dimensioni richieste per il buffer di script.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il numero di caratteri recuperati nel buffer di script, incluso il carattere Null di terminazione. Se la funzione ha esito positivo e il valore di *cchScripts* è 0, il valore restituito è la dimensione richiesta, in caratteri che includono un carattere Null di terminazione, per il buffer dello script.

Questa funzione restituisce 0 se non ha esito positivo. Per ottenere informazioni estese sull'errore, l'applicazione può chiamare [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), che può restituire uno dei codici di errore seguenti:

-   ERRORE \_ BADDB. La funzione non è stata in grado di accedere ai dati. Questa situazione in genere non deve verificarsi e indica in genere un'installazione non erta, un problema del disco o simili.
-   ERRORE \_ BUFFER \_ INSUFFICIENTE. Le dimensioni del buffer specificate non erano sufficienti o non erano impostate in modo errato su **NULL.**
-   ERRORE \_ PARAMETRO \_ NON VALIDO. Uno dei valori dei parametri non è valido.

## <a name="remarks"></a>Commenti

Questa funzione è utile come parte di una strategia per attenuare i problemi di sicurezza correlati ai nomi di dominio [internazionalizzati (IDN).](handling-internationalized-domain-names--idns.md)

Ecco alcuni esempi di input e output per questa funzione, presupponendo una dimensione del buffer sufficiente:



| Locale                  | *lpLocaleName* | *lpScripts*     |
|-------------------------|----------------|-----------------|
| Inglese (Stati Uniti) | it-IT          | Latn;           |
| Hindi (India)           | hi-IN          | Deva;           |
| Giapponese (Giappone)        | ja-JP          | Hani; Hira; Kana; |



 

L'elenco non contiene lo script latino, a meno che non sia una parte essenziale del sistema di scrittura usato per le impostazioni locali. Tuttavia, i caratteri latini vengono spesso usati nel contesto delle impostazioni locali per le quali non sono nativi, come per un nome commerciale estraneo. Nell'esempio precedente per Hindi in India, l'unico script recuperato è "Deva" (per Devanagari), anche se i caratteri latini possono essere visualizzati anche nel testo hindi. La [**funzione DownlevelVerifyScripts**](downlevelverifyscripts.md) ha un flag speciale per risolvere il caso specifico.

Il file di intestazione e la DLL necessari fanno parte del download ["MICROSOFT Internationalized Domain Name (IDN) Mitigation APIs",](https://www.microsoft.com/downloads/details.aspx?FamilyID=AD6158D7-DDBA-416A-9109-07607425A815&displaylang=en) disponibile nell'Area [download MSDN.](https://www.microsoft.com/?ref=go)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                                                                                                 |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                                                                                        |
| Componente ridistribuibile<br/>          | API di mitigazione IDN (Internationalized Domain Name) microsoft in Windows XP (SP2 o versione successiva), Windows Server 2003 (SP1 o versione successiva) o Windows Vista<br/> |
| Intestazione<br/>                   | <dl> <dt>Idndl.h</dt> </dl>                                                                          |
| DLL<br/>                      | <dl> <dt>Idndl.dll</dt> </dl>                                                                        |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Supporto linguistico nazionale](national-language-support.md)
</dt> <dt>

[Funzioni di supporto linguistico nazionale](national-language-support-functions.md)
</dt> <dt>

[Gestione dei nomi di dominio internazionalizzati (IDN)](handling-internationalized-domain-names--idns.md)
</dt> <dt>

[**DownlevelGetStringScripts**](downlevelgetstringscripts.md)
</dt> <dt>

[**DownlevelVerifyScripts**](downlevelverifyscripts.md)
</dt> <dt>

[**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa)
</dt> </dl>

 

 
