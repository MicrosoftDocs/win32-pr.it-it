---
description: Fornisce un elenco di script utilizzati nella stringa Unicode specificata.
ms.assetid: 3ad23613-8d0c-432a-b352-637c373a0980
title: Funzione DownlevelGetStringScripts (idndl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DownlevelGetStringScripts
api_type:
- DllExport
api_location:
- Idndl.dll
ms.openlocfilehash: bc5a9fdaf3beb9e1c401943f923fa48bd9d4b44c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317163"
---
# <a name="downlevelgetstringscripts-function"></a>DownlevelGetStringScripts (funzione)

Fornisce un elenco di script utilizzati nella stringa Unicode specificata.

> [!Note]  
> Questa funzione viene utilizzata solo dalle applicazioni eseguite in sistemi operativi precedenti a Windows Vista. Il relativo utilizzo richiede il pacchetto di download. Le applicazioni che vengono eseguite solo in Windows Vista e versioni successive devono chiamare [**GetStringScripts**](/windows/desktop/api/Winnls/nf-winnls-getstringscripts).

 

## <a name="syntax"></a>Sintassi


```C++
int DownlevelGetStringScripts(
  _In_  DWORD   dwFlags,
  _In_  LPCWSTR lpString,
  _In_  int     cchString,
  _Out_ LPWSTR  lpScripts,
  _In_  int     cchScripts
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Flag che specificano le opzioni per il recupero di script.



| Valore                                                                                                                                                                                                  | Significato                                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GSS_ALLOW_INHERITED_COMMON"></span><span id="gss_allow_inherited_common"></span><dl> <dt>**GSS \_ Consenti \_ ereditato \_ comune**</dt> </dl> | Recuperare le informazioni sullo script "Qaii" (ereditato) e "Rachele" (comune). Questo valore non influisce sull'elaborazione di caratteri non assegnati. Questi caratteri nella stringa di input determinano sempre la visualizzazione di un "ZZZZ" (script non assegnato) nella stringa di script.<br/> |



 

> [!Note]  
> Per impostazione predefinita, questa funzione ignora tutti i caratteri comuni o ereditati nella stringa Unicode di input. Se GSS \_ Consenti \_ ereditato \_ Common non è impostato, non verrà visualizzato né "Qaii" né "Rachele" nella stringa dello script, anche se la stringa di input contiene tali caratteri. Se GSS \_ Consenti \_ ereditato \_ Common è impostato e se la stringa di input contiene caratteri ereditati e/o comuni, nella stringa dello script vengono visualizzati "Qaii" e/o "Rachele". Vedere la sezione relativa alle osservazioni.

 

</dd> <dt>

*lpString* \[ in\]
</dt> <dd>

Puntatore alla stringa Unicode da analizzare.

</dd> <dt>

*cchString* \[ in\]
</dt> <dd>

Dimensione, in caratteri, della stringa Unicode indicata da *lpString*. L'applicazione imposta questo parametro su-1 se la stringa è con terminazione null. Se l'applicazione imposta questo parametro su 0, la funzione recupera una stringa Unicode null (L " \\ 0") in *lpScripts* e restituisce 1.

</dd> <dt>

*lpScripts* \[ out\]
</dt> <dd>

Puntatore a un buffer in cui questa funzione recupera una stringa a terminazione null che rappresenta un elenco di script, usando la notazione di 4 caratteri usata nello standard [ISO 15924](https://www.unicode.org/iso15924/iso15924-codes.html). Ogni nome di script è costituito da quattro caratteri latini e i nomi vengono recuperati in ordine alfabetico. Ogni nome, incluso l'ultimo, è seguito da un punto e virgola.

In alternativa, questo parametro può contenere **null** se *cchScripts* è impostato su 0. In questo caso, la funzione restituisce la dimensione richiesta per il buffer di script.

</dd> <dt>

*cchScripts* \[ in\]
</dt> <dd>

Dimensione, in caratteri, del buffer di script indicato da *lpScripts*.

In alternativa, l'applicazione può impostare questo parametro su 0. In questo caso, la funzione recupera il **valore null** in *lpScripts* e restituisce la dimensione richiesta per il buffer di script.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il numero di caratteri recuperati nel buffer di output, incluso un carattere di terminazione null, se ha esito positivo e *cchScripts* è impostato su un valore diverso da zero. La funzione restituisce 1 per indicare che non è stato trovato alcuno script, ad esempio quando la stringa di input contiene solo caratteri comuni o EREDITAti e GSS \_ Consenti \_ ereditato \_ comune non è impostato. Dato che ogni script trovato aggiunge cinque caratteri (quattro caratteri + delimitatore), una semplice operazione matematica fornisce il conteggio degli script come ( \_ codice restituito-1)/5.

Se la funzione ha esito positivo e il valore di *cchScripts* è 0, il valore restituito è la dimensione richiesta, in caratteri che include un carattere null di terminazione, per il buffer di script. Il numero di script è come descritto in precedenza.

Se l'operazione non riesce, la funzione restituisce 0. Per ottenere informazioni estese sull'errore, l'applicazione può chiamare [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), che può restituire uno dei codici di errore seguenti:

-   ERRORE \_ BADDB. La funzione non è stata in grado di accedere ai dati. Questa situazione non dovrebbe in genere verificarsi e in genere indica un'installazione non valida, un problema del disco o un tipo simile.
-   ERRORE \_ \_ nel buffer insufficiente. Una dimensione del buffer specificata non è sufficientemente grande oppure è stata impostata erroneamente su **null**.
-   flag di errore \_ non validi \_ . I valori specificati per i flag non sono validi.
-   ERRORE \_ parametro non valido \_ . Uno dei valori di parametro non è valido.

## <a name="remarks"></a>Commenti

Questa funzione è utile come parte di una strategia per attenuare i problemi di sicurezza correlati ai [nomi di dominio internazionali (IDN)](handling-internationalized-domain-names--idns.md).

La determinazione degli script si basa sui valori di script pubblicati dal Consorzio Unicode in <https://www.unicode.org/Public/4.1.0/ucd/Scripts.txt> , ad eccezione del fatto che i caratteri non assegnati hanno il valore "ZZZZ" (non assegnato) invece di "Rachele" (comune).

Di seguito sono riportati alcuni esempi del comportamento di questa funzione:



Stringa di input

*dwFlags*

*lpScripts*

Script

Microsoft.com

0

Latn

Latino

Microsoft.com

GSS \_ Consenti \_ ereditato \_ comune

Latn Rachele

Latino + comune

$ {ROWSPAN2} $Ni ño $ {REMOVE} $  

004E 0069 0241 006F

$ {ROWSPAN2} $GSS \_ consentire \_ il \_ comune ereditato $ {Remove} $  

$ {ROWSPAN2} $Latn; $ {REMOVE} $  

$ {ROWSPAN2} $Latin $ {REMOVE} $  

Usa la lettera latina MINUSCOLa N con TILDE

$ {ROWSPAN2} $Ni ño $ {REMOVE} $  

004E 0069 006E 0303 006F

$ {ROWSPAN2} $GSS \_ consentire \_ il \_ comune ereditato $ {Remove} $  

$ {ROWSPAN2} $Latn; Qaii; $ {REMOVE} $  

$ {ROWSPAN2} $Latin + ereditato $ {REMOVE} $  

Usa la combinazione TILDE

$ {ROWSPAN2} $Sp ооf $ {REMOVE} $  

0053 0070 043e 043e 0066

$ {ROWSPAN2} $0 $ {REMOVE} $  

$ {ROWSPAN2} $Latn; Cyrl; $ {REMOVE} $  

$ {ROWSPAN2} $Latin + Cirillico $ {REMOVE} $  

Usa la lettera MINUSCOLa cirillico O



U + F000

0

ZZZZ

Unassigned (Non assegnato)



U + F000

GSS \_ Consenti \_ ereditato \_ comune

ZZZZ

Unassigned (Non assegnato)



 

Il file di intestazione e la DLL necessari fanno parte del download di ["API di mitigazione del nome di dominio Microsoft (IDN)"](https://www.microsoft.com/downloads/details.aspx?FamilyID=AD6158D7-DDBA-416A-9109-07607425A815&displaylang=en%0A) , disponibile nell' [area download MSDN](https://www.microsoft.com/?ref=go).

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

[**DownlevelGetLocaleScripts**](downlevelgetlocalescripts.md)
</dt> <dt>

[**DownlevelVerifyScripts**](downlevelverifyscripts.md)
</dt> <dt>

[**GetStringScripts**](/windows/desktop/api/Winnls/nf-winnls-getstringscripts)
</dt> </dl>

 

 
