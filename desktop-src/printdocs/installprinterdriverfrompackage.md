---
description: Installa un driver della stampante da un pacchetto driver presente nell'archivio driver dei server di stampa.
ms.assetid: 5906d9c6-9fbf-4ec6-81ce-112a9ef6d7c0
title: Funzione InstallPrinterDriverFromPackage (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InstallPrinterDriverFromPackage
- InstallPrinterDriverFromPackageA
- InstallPrinterDriverFromPackageW
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: f817f5e73537f6a71d8236ad9532acdf02a53552
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233724"
---
# <a name="installprinterdriverfrompackage-function"></a>InstallPrinterDriverFromPackage (funzione)

Installa un driver della stampante da un pacchetto driver presente nell'archivio driver del server di stampa.

## <a name="syntax"></a>Sintassi


```C++
HRESULT InstallPrinterDriverFromPackage(
  _In_ LPCTSTR pszServer,
  _In_ LPCTSTR pszInfPath,
  _In_ LPCTSTR pszDriverName,
  _In_ LPCTSTR pszEnvironment,
  _In_ DWORD   dwFlags
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pszServer* \[ in\]
</dt> <dd>

Puntatore a una stringa costante a terminazione null che specifica il nome del server di stampa. **Null** indica il computer locale.

</dd> <dt>

*pszInfPath* \[ in\]
</dt> <dd>

Puntatore a una stringa costante a terminazione null che specifica il percorso dell'archivio driver per il file. inf del driver di stampa. **Null** indica che il driver si trova in un file inf fornito con Windows.

</dd> <dt>

*pszDriverName* \[ in\]
</dt> <dd>

Puntatore a una stringa costante a terminazione null che specifica il nome del driver.

</dd> <dt>

*pszEnvironment* \[ in\]
</dt> <dd>

Puntatore a una stringa costante a terminazione null che specifica l'architettura del processore, ad esempio Windows NT x86. Può essere **null**.

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Questo può essere solo 0 o IPDFP \_ Copia \_ tutti \_ i file. Il valore 0 indica che è necessario aggiungere il driver della stampante ed è necessario copiare tutti i file nella directory del driver della stampante più recenti rispetto ai file corrispondenti attualmente in uso. Il valore IPDFP \_ copy \_ All \_ files indica che è necessario aggiungere il driver della stampante e tutti i file nella directory del driver della stampante. I timestamp del file vengono ignorati quando *dwFlags* ha un valore IPDFP \_ Copia \_ tutti \_ i file.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se l'operazione ha esito positivo, il valore restituito è \_ OK, altrimenti **HRESULT** conterrà un codice di errore.

Per ulteriori informazioni sui codici di errore COM, vedere [gestione degli errori](../com/error-handling-in-com.md).

## <a name="remarks"></a>Commenti

> [!Note]  
> Si tratta di una funzione di blocco o sincrona e potrebbe non essere restituita immediatamente. La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione. La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.

 

L'archivio driver è in genere% windir% \\ inf o% windir% \\ system32 \\ DriverStore \\ FileRepository.

**InstallPrinterDriverFromPackage** installa anche altri file nel pacchetto, ad esempio i profili colori e i processori di stampa.

Gli utenti devono disporre dei diritti di amministrazione della stampante per installare in un computer remoto o nel computer locale quando l'utente è connesso con Servizi terminal.

Solo i pacchetti firmati possono essere installati in un computer remoto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool. h (include Windows. h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Spoolss.dll</dt> </dl>                    |
| Nomi Unicode e ANSI<br/>   | **InstallPrinterDriverFromPackageW** (Unicode) e **InstallPrinterDriverFromPackageA** (ANSI)<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Funzioni dell'API spooler di stampa](printing-and-print-spooler-functions.md)
</dt> </dl>

 

