---
description: Il metodo IWiaDevMgr2::GetImageDlg visualizza una o più finestre di dialogo che consentono a un utente di acquisire un'immagine da un dispositivo WIA (Windows Image Acquisition) 2.0 e scrivere l'immagine in un file specificato.
ms.assetid: 30a63426-150e-44cf-a03e-7b6da14450f7
title: Metodo IWiaDevMgr2::GetImageDlg (Wia.h)
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
ms.openlocfilehash: 0b03356e40f1c708c852917c890e4c1bf96b98cd18ccf82b75ebcaaccaa69597
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119814041"
---
# <a name="iwiadevmgr2getimagedlg-method"></a>Metodo IWiaDevMgr2::GetImageDlg

Il metodo **IWiaDevMgr2::GetImageDlg** visualizza una o più finestre di dialogo che consentono a un utente di acquisire un'immagine da un dispositivo WIA (Windows Image Acquisition) 2.0 e scrivere l'immagine in un file specificato. Questo metodo estende la funzionalità di [**IWiaDevMgr2::SelectDeviceDlg**](-wia-iwiadevmgr2-selectdevicedlg.md) per incapsulare l'acquisizione di immagini all'interno di una singola chiamata API.

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

*lFlags* \[ Pollici\]
</dt> <dd>

Tipo: **LONG**

Specifica il comportamento della finestra di dialogo. È possibile impostare i valori seguenti:



| Contrassegno                                 | Significato                                                                                                                                                                     |
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0                                    | Comportamento predefinito.                                                                                                                                                           |
| FINESTRA DI DIALOGO DEL DISPOSITIVO WIA \_ \_ USA \_ \_ L'INTERFACCIA \_ UTENTE COMUNE | Usare l'interfaccia utente del sistema anziché l'interfaccia utente fornita dal fornitore. Se l'interfaccia utente del sistema non è disponibile, viene usata l'interfaccia utente del fornitore. Se nessuna delle due interfaccia utente è disponibile, la funzione restituisce E \_ NOTIMPL. |



 

</dd> <dt>

*bstrDeviceID* \[ Pollici\]
</dt> <dd>

Tipo: **BSTR**

Specifica lo scanner da usare.

</dd> <dt>

*hwndParent* \[ Pollici\]
</dt> <dd>

Tipo: **HWND**

Handle della finestra proprietaria della finestra **di** dialogo Ottieni immagine.

</dd> <dt>

*bstrFolderName* \[ Pollici\]
</dt> <dd>

Tipo: **BSTR**

Specifica il nome della cartella in cui vengono archiviati i file analizzati.

</dd> <dt>

*bstrFilename* \[ Pollici\]
</dt> <dd>

Tipo: **BSTR**

Specifica il nome del file in cui scrivere i dati dell'immagine.

</dd> <dt>

*plNumFiles* \[ Pollici\]
</dt> <dd>

Tipo: **\* LONG**

Puntatore al numero di file da analizzare.

</dd> <dt>

*ppbstrFilePaths* \[ Pollici\]
</dt> <dd>

Tipo: **BSTR \* \***

Indirizzo di un puntatore a una matrice di percorsi per i file analizzati. Inizializzare il puntatore in modo che punti a una matrice di dimensioni zero (0) prima che venga chiamato **IWiaDevMgr2::GetImageDlg.** Vedere **Note**.

</dd> <dt>

*ppItem* \[ in, out\]
</dt> <dd>

Tipo: **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***

Indirizzo di un puntatore a [**IWiaItem2**](-wia-iwiaitem2.md) da cui sono state analizzate le immagini.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

**IWiaDevMgr2::GetImageDlg** restituisce S OK se i dati vengono trasferiti correttamente, restituisce S FALSE se l'utente annulla la finestra di dialogo o restituisce un errore \_ \_ COM standard.

> [!Note]  
> Il *parametro ppbstrFilePaths* non è necessariamente vuoto, se la funzione restituisce S \_ FALSE. Se l'utente annulla, le pagine che hanno completato l'analisi vengono elaborate e restituite in *ppbstrFilePaths*. Anche se non vengono usati, è necessario liberare la matrice. Vedere **Note**.

 

## <a name="remarks"></a>Commenti

Se l'applicazione passa **NULL** per il valore del parametro *bstrDeviceID,* **IWiaDevMgr2::GetImageDlg** visualizza la finestra di dialogo Seleziona dispositivo in modo che l'utente possa selezionare il dispositivo di input WIA 2.0. 

Usare una voce di menu denominata **Da scanner** nel menu **File** in modo che le selezioni di dispositivi e immagini siano disponibili nell'applicazione.

Chiamare [SysFreeString](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring) su ogni BSTR nella matrice a cui *punta ppbstrFilePaths* \[ i e chiamare \] [CoTaskMemFree](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) sulla matrice stessa per liberare la memoria associata. Se viene restituito S FALSE, verificare se il valore a cui \_ *punta plNumFiles* è diverso da zero. Se il valore è diverso da zero, liberare le risorse *ppbstrFilePaths* i nell'applicazione, perché l'utente potrebbe annullare l'operazione dopo l'analisi di una \[ o più \] pagine. Inizializzare *plNumFiles* su zero prima di chiamare **IWiaDevMgr2::GetImageDlg**. Se *plNumFiles* non viene inizializzato su zero e un errore nell'infrastruttura COM fa sì che la funzione restituirà S FALSE prima che venga chiamato \_ **IWiaDevMgr2::GetImageDlg,** *plNumFiles* avrà un valore fuorviante di Garbage Collection.

La finestra di dialogo deve avere diritti sufficienti per *bstrFolderName* in modo da poter salvare i file con nomi di file univoci. Proteggere la cartella con un elenco di controllo di accesso (ACL) perché contiene dati utente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                   |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>Wia.h</dt> </dl> |



 

 
