---
description: Installa un driver della stampante da un pacchetto driver presente nell'archivio driver dei server di stampa.
ms.assetid: 5906d9c6-9fbf-4ec6-81ce-112a9ef6d7c0
title: Funzione InstallPrinterDriverFromPackage (Winspool.h)
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
ms.openlocfilehash: 3248fc1a2392e2a04fd83c58ddcc08a110eec94779b634ce6a348639d4d2a5c2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120112471"
---
# <a name="installprinterdriverfrompackage-function"></a>Funzione InstallPrinterDriverFromPackage

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

*pszServer* \[ Pollici\]
</dt> <dd>

Puntatore a una stringa costante con terminazione Null che specifica il nome del server di stampa. **NULL** indica il computer locale.

</dd> <dt>

*pszInfPath* \[ Pollici\]
</dt> <dd>

Puntatore a una stringa costante con terminazione Null che specifica il percorso dell'archivio driver per il file inf del driver di stampa. **NULL** indica che il driver si trova in un file inf fornito con Windows.

</dd> <dt>

*pszDriverName* \[ Pollici\]
</dt> <dd>

Puntatore a una stringa costante con terminazione Null che specifica il nome del driver.

</dd> <dt>

*pszEnvironment* \[ Pollici\]
</dt> <dd>

Puntatore a una stringa costante con terminazione Null che specifica l'architettura del processore, ad esempio Windows NT x86. Può essere **NULL.**

</dd> <dt>

*dwFlags* \[ Pollici\]
</dt> <dd>

Può essere solo 0 o IPDFP \_ COPY \_ ALL \_ FILES. Il valore 0 indica che è necessario aggiungere il driver della stampante e copiare tutti i file nella directory del driver della stampante più recente rispetto ai file corrispondenti attualmente in uso. Il valore IPDFP COPY ALL FILES indica che è necessario aggiungere il driver della stampante e tutti i file nella directory del \_ \_ driver della \_ stampante. I timestamp dei file vengono ignorati *quando dwFlags* ha valore IPDFP \_ COPY ALL \_ \_ FILES.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se l'operazione ha esito positivo, il valore restituito è S OK, in caso contrario \_ **HRESULT** conterrà un codice di errore.

Per altre informazioni sui codici di errore COM, vedere [Gestione degli errori](../com/error-handling-in-com.md).

## <a name="remarks"></a>Commenti

> [!Note]  
> Si tratta di una funzione di blocco o sincrona e potrebbe non restituire immediatamente . La velocità di ritorno di questa funzione dipende da fattori in fase di esecuzione, ad esempio lo stato di rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione. La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non rispetti.

 

L'archivio driver è in genere %windir% \\ inf o %windir% \\ System32 \\ DriverStore \\ FileRepository.

**InstallPrinterDriverFromPackage** installa anche altri file nel pacchetto, ad esempio profili colori e processori di stampa.

Gli utenti devono disporre dei diritti di amministrazione della stampante per l'installazione in un computer remoto o nel computer locale quando l'utente è connesso con Servizi terminal.

Solo i pacchetti firmati possono essere installati in un computer remoto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                                            |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Spoolss.dll</dt> </dl>                    |
| Nomi Unicode e ANSI<br/>   | **InstallPrinterDriverFromPackageW** (Unicode) e **InstallPrinterDriverFromPackageA** (ANSI)<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Funzioni dell'API spooler di stampa](printing-and-print-spooler-functions.md)
</dt> </dl>

 

