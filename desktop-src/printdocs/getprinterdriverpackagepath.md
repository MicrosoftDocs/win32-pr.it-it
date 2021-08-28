---
description: Recupera il percorso del pacchetto driver della stampante specificato in un server di stampa.
ms.assetid: e88e984b-d2c0-43b4-8f70-b05ec202ab14
title: Funzione GetPrinterDriverPackagePath (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrinterDriverPackagePath
- GetPrinterDriverPackagePathA
- GetPrinterDriverPackagePathW
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 5058d57a0275019c5e603673d260c9969cc0b5d5641dea15e09ffe242addff10
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119600801"
---
# <a name="getprinterdriverpackagepath-function"></a>Funzione GetPrinterDriverPackagePath

Recupera il percorso del pacchetto driver della stampante specificato in un server di stampa.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetPrinterDriverPackagePath(
  _In_    LPCTSTR pszServer,
  _In_    LPCTSTR pszEnvironment,
  _In_    LPCTSTR pszLanguage,
  _In_    LPCTSTR pszPackageID,
  _Inout_ LPTSTR  pszDriverPackageCab,
  _In_    DWORD   cchDriverPackageCab,
  _Out_   LPDWORD pcchRequiredSize
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pszServer* \[ Pollici\]
</dt> <dd>

Puntatore a una stringa costante con terminazione Null che specifica il nome del server di stampa. Usare **NULL** per il computer locale.

</dd> <dt>

*pszEnvironment* \[ Pollici\]
</dt> <dd>

Puntatore a una stringa costante con terminazione Null che specifica l'architettura del processore, ad esempio Windows NT x86. Può essere **NULL.**

</dd> <dt>

*pszLanguage* \[ Pollici\]
</dt> <dd>

Puntatore a una stringa costante con terminazione Null che specifica la [lingua interfaccia utente multilingue](/windows/desktop/Intl/mui-resource-management) per il driver da installare. Può essere **NULL.**

</dd> <dt>

*pszPackageID* \[ Pollici\]
</dt> <dd>

Puntatore a una stringa costante con terminazione Null che specifica l'ID del pacchetto driver.

</dd> <dt>

*pszDriverPackageCab* \[ in, out\]
</dt> <dd>

Puntatore a una stringa con terminazione Null che specifica il percorso del file CAB per il pacchetto driver. Può essere **NULL.** Vedere la sezione Osservazioni.

</dd> <dt>

*cchDriverPackageCab* \[ Pollici\]
</dt> <dd>

Dimensione, in caratteri, del buffer *pszDriverPackageCab.* Può essere **NULL.**

</dd> <dt>

*pcchRequiredSize* \[ Cambio\]
</dt> <dd>

Puntatore alla dimensione richiesta del buffer *pszDriverPackageCab.*

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se l'operazione ha esito positivo, il valore restituito è S OK. In \_ caso contrario, **HRESULT** conterrà un codice di errore.

Per altre informazioni sui codici di errore COM, vedere [Gestione degli errori.](../com/error-handling-in-com.md)

## <a name="remarks"></a>Commenti

> [!Note]  
> Si tratta di una funzione di blocco o sincrona che potrebbe non essere restituita immediatamente. La velocità di ritorno di questa funzione dipende da fattori di run-time, ad esempio lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante, difficili da prevedere durante la scrittura di un'applicazione. La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non rispetti.

 

Per ottenere un valore per *cchDriverPackageCab,* chiamare la funzione con **NULL** come valore di *pszDriverPackageCab*. Usare il valore restituito in *pcchRequiredSize* come valore di *cchDriverPackageCab* e chiamare di nuovo la funzione.

*PszPackageID viene* in genere ottenuto da una chiamata a [**GetCorePrinterDrivers.**](getcoreprinterdrivers.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                                            |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool.h (includere Windows.h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Spoolss.dll</dt> </dl>                    |
| Nomi Unicode e ANSI<br/>   | **GetPrinterDriverPackagePathW** (Unicode) e **GetPrinterDriverPackagePathA** (ANSI)<br/>         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Funzioni dell'API spooler di stampa](printing-and-print-spooler-functions.md)
</dt> </dl>

 

