---
description: "Il metodo IWiaDevMgr2:: GetImageDlg Visualizza una o più finestre di dialogo che consentono a un utente di acquisire un'immagine da un dispositivo Windows Image Acquisition (WIA) 2,0 e di scrivere l'immagine in un file specificato."
ms.assetid: 30a63426-150e-44cf-a03e-7b6da14450f7
title: 'Metodo IWiaDevMgr2:: GetImageDlg (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaDevMgr2.GetImageDlg
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 6777b839beeb809383e524960e8882392be4bd24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312417"
---
# <a name="iwiadevmgr2getimagedlg-method"></a>Metodo IWiaDevMgr2:: GetImageDlg

Il metodo **IWiaDevMgr2:: GetImageDlg** Visualizza una o più finestre di dialogo che consentono a un utente di acquisire un'immagine da un dispositivo Windows Image Acquisition (WIA) 2,0 e di scrivere l'immagine in un file specificato. Questo metodo estende la funzionalità di [**IWiaDevMgr2:: SelectDeviceDlg**](-wia-iwiadevmgr2-selectdevicedlg.md) per incapsulare l'acquisizione di immagini in una singola chiamata API.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetImageDlg(
  [in]      LONG      lFlags,
  [in]      BSTR      bstrDeviceID,
  [in]      HWND      hwndParent,
  [in]      BSTR      bstrFolderName,
  [in]      BSTR      bstrFilename,
  [in]      LONG      *plNumFiles,
  [in]      BSTR      **ppbstrFilePaths,
  [in, out] IWiaItem2 **ppItem
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*è* \[ in\]
</dt> <dd>

Tipo: **Long**

Specifica il comportamento della finestra di dialogo. Può essere impostato sui valori seguenti:



| Contrassegno                                 | Significato                                                                                                                                                                     |
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0                                    | Comportamento predefinito.                                                                                                                                                           |
| \_finestra di dialogo del dispositivo WIA usare l' \_ \_ \_ \_ interfaccia utente comune | Utilizzare l'interfaccia utente del sistema anziché l'interfaccia utente fornita dal fornitore. Se l'interfaccia utente del sistema non è disponibile, viene utilizzata l'interfaccia utente del fornitore. Se nessuna delle due interfacce è disponibile, la funzione restituisce E \_ NOTIMPL. |



 

</dd> <dt>

*bstrDeviceID* \[ in\]
</dt> <dd>

Tipo: **BSTR**

Specifica lo scanner da usare.

</dd> <dt>

*hwndParent* \[ in\]
</dt> <dd>

Tipo: **HWND**

Handle della finestra che possiede la finestra di dialogo **Ottieni immagine** .

</dd> <dt>

*bstrFolderName* \[ in\]
</dt> <dd>

Tipo: **BSTR**

Specifica il nome della cartella in cui sono archiviati i file analizzati.

</dd> <dt>

*bstrFilename* \[ in\]
</dt> <dd>

Tipo: **BSTR**

Specifica il nome del file in cui scrivere i dati dell'immagine.

</dd> <dt>

*plNumFiles* \[ in\]
</dt> <dd>

Tipo: **Long \** _

Puntatore al numero di file da analizzare.

</dd> <dt>

_ppbstrFilePaths * \[ in\]
</dt> <dd>

Tipo: **BSTR \* \***

Indirizzo di un puntatore a una matrice di percorsi per i file analizzati. Inizializzare il puntatore in modo che punti a una matrice di dimensioni zero (0) prima di chiamare **IWiaDevMgr2:: GetImageDlg** . Vedere la **sezione Osservazioni**.

</dd> <dt>

*ppItem* \[ in uscita\]
</dt> <dd>

Tipo: **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***

Indirizzo di un puntatore a [**IWiaItem2**](-wia-iwiaitem2.md) da cui sono state analizzate le immagini.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

**IWiaDevMgr2:: GetImageDlg** restituisce \_ OK se i dati vengono trasferiti correttamente, restituisce \_ false se l'utente annulla la finestra di dialogo o restituisce un errore com standard.

> [!Note]  
> Il parametro *ppbstrFilePaths* non è necessariamente vuoto, se la funzione restituisce \_ false. Se l'utente Annulla, le pagine che hanno completato l'analisi vengono elaborate e restituite in *ppbstrFilePaths*. Anche se non vengono usati, è necessario liberare la matrice. Vedere la **sezione Osservazioni**.

 

## <a name="remarks"></a>Commenti

Se l'applicazione passa **null** come valore del parametro *bstrDeviceID* , **IWiaDevMgr2:: GetImageDlg** Visualizza la finestra di dialogo **Seleziona dispositivo** in modo che l'utente possa selezionare il dispositivo di input WIA 2,0.

Usare una voce di menu denominata **da scanner** nel menu **file** per fare in modo che le selezioni del dispositivo e dell'immagine siano disponibili nell'applicazione.

Chiamare [SysFreeString](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring) per ogni BSTR nella matrice a cui  \[ punta ppbstrFilePaths \] e chiamare [CoTaskMemFree](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) sulla matrice stessa per liberare la memoria associata. Se \_ viene restituito S false, verificare se il valore a cui punta *plNumFiles* è diverso da zero. Se il valore è diverso da zero, liberare le risorse *ppbstrFilePaths* \[ i \] nell'applicazione, in quanto l'utente può annullare l'operazione dopo aver analizzato una o più pagine. Inizializzare *plNumFiles* su zero prima di chiamare **IWiaDevMgr2:: GetImageDlg**. Se *plNumFiles* non è inizializzato su zero e un errore nell'infrastruttura com fa in modo che la funzione restituisca S \_ false prima di **IWiaDevMgr2:: GetImageDlg** viene chiamato, *plNumFiles* avrà un valore di Garbage Collection fuorviante.

La finestra di dialogo deve disporre di diritti sufficienti per *bstrFolderName* , in modo che sia possibile salvare i file con nomi file univoci. Proteggere la cartella con un elenco di controllo di accesso (ACL) perché contiene dati utente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                   |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>WIA. h</dt> </dl> |



 

 
