---
description: Fornisce un elenco di script per le impostazioni locali specificate.
ms.assetid: 0cedcf6c-bab4-4e0f-ab8f-04aa8e51602f
title: Funzione DownlevelGetLocaleScripts (idndl. h)
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
ms.openlocfilehash: f636ab426cd4d50878df93e3e30d69de54d60ac6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233310"
---
# <a name="downlevelgetlocalescripts-function"></a>DownlevelGetLocaleScripts (funzione)

Fornisce un elenco di script per le impostazioni locali specificate.

> [!Note]  
> Questa funzione viene utilizzata solo dalle applicazioni eseguite in sistemi operativi precedenti a Windows Vista. Il relativo utilizzo richiede il pacchetto di download. Le applicazioni che vengono eseguite solo in Windows Vista e versioni successive devono chiamare [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) con *LCType* impostato su [locale \_ SSCRIPTS](locale-sscripts.md).

 

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

*lpLocaleName* \[ in\]
</dt> <dd>

Puntatore a un [nome delle impostazioni locali](locale-names.md)con terminazione null.

</dd> <dt>

*lpScripts* \[ out\]
</dt> <dd>

Puntatore a un buffer in cui questa funzione recupera una stringa a terminazione null che rappresenta un elenco di script, usando la notazione di 4 caratteri usata nello standard [ISO 15924](https://www.unicode.org/iso15924/iso15924-codes.html). Ogni nome di script è costituito da quattro caratteri latini e i nomi vengono recuperati in ordine alfabetico. Ognuno di essi, incluso l'ultimo, è seguito da un punto e virgola.

In alternativa, questo parametro può contenere **null** se *cchScripts* è impostato su 0. In questo caso, la funzione restituisce la dimensione richiesta per il buffer di script.

</dd> <dt>

*cchScripts* \[ in\]
</dt> <dd>

Dimensione, in caratteri, del buffer di script indicato da *lpScripts*.

In alternativa, l'applicazione può impostare questo parametro su 0. In questo caso, la funzione recupera il **valore null** in *lpScripts* e restituisce la dimensione richiesta per il buffer di script.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il numero di caratteri recuperati nel buffer di script, incluso il carattere null di terminazione. Se la funzione ha esito positivo e il valore di *cchScripts* è 0, il valore restituito è la dimensione richiesta, in caratteri che include un carattere null di terminazione, per il buffer di script.

Questa funzione restituisce 0 in caso di esito negativo. Per ottenere informazioni estese sull'errore, l'applicazione può chiamare [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), che può restituire uno dei codici di errore seguenti:

-   ERRORE \_ BADDB. La funzione non è stata in grado di accedere ai dati. Questa situazione non dovrebbe in genere verificarsi e in genere indica un'installazione non valida, un problema del disco o un tipo simile.
-   ERRORE \_ \_ nel buffer insufficiente. Una dimensione del buffer specificata non è sufficientemente grande oppure è stata impostata erroneamente su **null**.
-   ERRORE \_ parametro non valido \_ . Uno dei valori di parametro non è valido.

## <a name="remarks"></a>Commenti

Questa funzione è utile come parte di una strategia per attenuare i problemi di sicurezza correlati ai [nomi di dominio internazionali (IDN)](handling-internationalized-domain-names--idns.md).

Di seguito sono riportati alcuni esempi di input e output per questa funzione, presumendo una dimensione del buffer sufficiente:



| Locale                  | *lpLocaleName* | *lpScripts*     |
|-------------------------|----------------|-----------------|
| Inglese (Stati Uniti) | it-IT          | Latn           |
| Hindi (India)           | hi-IN          | Deva           |
| Giapponese (Giappone)        | ja-JP          | Hani Hira Kana |



 

L'elenco non contiene lo script latino, a meno che non si tratti di una parte essenziale del sistema di scrittura usato per le impostazioni locali. Tuttavia, i caratteri latini vengono spesso usati nel contesto delle impostazioni locali per cui non sono nativi, come per un nome aziendale esterno. Nell'esempio precedente per hindi in India, l'unico script recuperato è "Deva" (per devangato), anche se i caratteri latini possono anche essere visualizzati in testo Hindi. La funzione [**DownlevelVerifyScripts**](downlevelverifyscripts.md) ha un flag speciale per risolvere il caso.

Il file di intestazione e la DLL necessari fanno parte del download di ["API di mitigazione del nome di dominio Microsoft (IDN)"](https://www.microsoft.com/downloads/details.aspx?FamilyID=AD6158D7-DDBA-416A-9109-07607425A815&displaylang=en) , disponibile nell' [area download MSDN](https://www.microsoft.com/?ref=go).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                                                                                                 |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                                                                        |
| Componente ridistribuibile<br/>          | API di mitigazione Microsoft per il nome di dominio internazionale (IDN) in Windows XP (SP2 o versioni successive), Windows Server 2003 (SP1 o versione successiva) o Windows Vista<br/> |
| Intestazione<br/>                   | <dl> <dt>Idndl. h</dt> </dl>                                                                          |
| DLL<br/>                      | <dl> <dt>Idndl.dll</dt> </dl>                                                                        |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Supporto per lingua nazionale](national-language-support.md)
</dt> <dt>

[Funzioni di supporto del linguaggio nazionale](national-language-support-functions.md)
</dt> <dt>

[Gestione dei nomi di dominio internazionalizzati (IDN)](handling-internationalized-domain-names--idns.md)
</dt> <dt>

[**DownlevelGetStringScripts**](downlevelgetstringscripts.md)
</dt> <dt>

[**DownlevelVerifyScripts**](downlevelverifyscripts.md)
</dt> <dt>

[**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa)
</dt> </dl>

 

 
