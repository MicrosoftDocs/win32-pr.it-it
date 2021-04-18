---
description: Recupera il percorso del pacchetto di driver della stampante specificato in un server di stampa.
ms.assetid: e88e984b-d2c0-43b4-8f70-b05ec202ab14
title: Funzione GetPrinterDriverPackagePath (winspool. h)
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
ms.openlocfilehash: ea355782df6cce7910f92a46af3cde320536106e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318380"
---
# <a name="getprinterdriverpackagepath-function"></a>GetPrinterDriverPackagePath (funzione)

Recupera il percorso del pacchetto di driver della stampante specificato in un server di stampa.

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

*pszServer* \[ in\]
</dt> <dd>

Puntatore a una stringa costante a terminazione null che specifica il nome del server di stampa. Utilizzare **null** per il computer locale.

</dd> <dt>

*pszEnvironment* \[ in\]
</dt> <dd>

Puntatore a una stringa costante a terminazione null che specifica l'architettura del processore, ad esempio Windows NT x86. Può essere **null**.

</dd> <dt>

*pszLanguage* \[ in\]
</dt> <dd>

Puntatore a una stringa costante a terminazione null che specifica la lingua dell' [interfaccia utente multilingue](/windows/desktop/Intl/mui-resource-management) per il driver da installare. Può essere **null**.

</dd> <dt>

*pszPackageID* \[ in\]
</dt> <dd>

Puntatore a una stringa costante a terminazione null che specifica l'ID del pacchetto driver.

</dd> <dt>

*pszDriverPackageCab* \[ in uscita\]
</dt> <dd>

Puntatore a una stringa con terminazione null che specifica il percorso del file CAB per il pacchetto driver. Può essere **null**. Vedere la sezione Osservazioni.

</dd> <dt>

*cchDriverPackageCab* \[ in\]
</dt> <dd>

Dimensione, in caratteri, del buffer *pszDriverPackageCab* . Può essere **null**.

</dd> <dt>

*pcchRequiredSize* \[ out\]
</dt> <dd>

Puntatore alla dimensione richiesta del buffer *pszDriverPackageCab* .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se l'operazione ha esito positivo, il valore restituito è \_ OK, altrimenti **HRESULT** conterrà un codice di errore.

Per ulteriori informazioni sui codici di errore COM, vedere [gestione degli errori](../com/error-handling-in-com.md).

## <a name="remarks"></a>Commenti

> [!Note]  
> Si tratta di una funzione di blocco o sincrona e potrebbe non essere restituita immediatamente. La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione. La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.

 

Per ottenere un valore per *cchDriverPackageCab*, chiamare la funzione con **null** come valore di *pszDriverPackageCab*. Usare il valore restituito in *pcchRequiredSize* come valore di *cchDriverPackageCab* e chiamare di nuovo la funzione.

*PszPackageID* viene in genere ottenuto da una chiamata a [**GetCorePrinterDrivers**](getcoreprinterdrivers.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool. h (include Windows. h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Spoolss.dll</dt> </dl>                    |
| Nomi Unicode e ANSI<br/>   | **GetPrinterDriverPackagePathW** (Unicode) e **GetPrinterDriverPackagePathA** (ANSI)<br/>         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Funzioni dell'API spooler di stampa](printing-and-print-spooler-functions.md)
</dt> </dl>

 

