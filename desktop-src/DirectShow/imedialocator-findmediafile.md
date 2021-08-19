---
description: Il metodo FindMediaFile cerca un file e, in caso di esito positivo, recupera il percorso del file.
ms.assetid: ddfa2c75-e51f-4aad-afe6-8a60c46e8d35
title: Metodo IMediaLocator::FindMediaFile (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaLocator.FindMediaFile
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: cc1acda4a3bc6e2d93ae8b7024ef34f759c11c5c4d487a09d3be3a3542e0c445
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117818938"
---
# <a name="imedialocatorfindmediafile-method"></a>Metodo IMediaLocator::FindMediaFile

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future Windows.\]

 

Il metodo cerca un file e, in caso di esito `FindMediaFile` positivo, recupera il percorso del file.

## <a name="syntax"></a>Sintassi


```C++
HRESULT FindMediaFile(
   BSTR Input,
   BSTR FilterString,
   BSTR *pOutput,
   long Flags
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Input* 
</dt> <dd>

Nome file, incluso il percorso, in cui si trova l'ultimo file noto. Per gli oggetti di origine nella sequenza temporale, usare il nome del supporto corrente.

</dd> <dt>

*FilterString* 
</dt> <dd>

Oggetto **BSTR contenente** coppie di stringhe di filtro, formattate come richiesto dal membro **lpstrFilter** della [**struttura OPENFILENAME.**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) Il localizzatore multimediale usa questo filtro se viene visualizzata una finestra di dialogo Apri file. Il valore può essere **NULL** se il *parametro Flags* non include il flag POPUP SFN \_ \_ VALIDATEF.

</dd> <dt>

*pOutput* 
</dt> <dd>

Puntatore a una variabile che riceve il percorso effettivo del file, se differisce dal valore contenuto in *Input* e se il metodo individua correttamente il file.

</dd> <dt>

*Flag* 
</dt> <dd>

Combinazione bit per bit di zero o più flag. Per un elenco dei flag possibili, vedere [**Flag di convalida dei nomi file**](file-name-validation-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

La stringa di filtro per la finestra di dialogo Apri file, specificata dal *parametro FilterString,* contiene caratteri Null interni. Ad esempio, Video \\ 0 \*.avi\\ 0 \\ 0 è una stringa di filtro valida. Non è possibile usare la **funzione SysAllocStr** per allocare BSTR, perché tale funzione prevede una stringa con terminazione Null e tronca la stringa in corrispondenza del primo carattere Null. Usare quindi una funzione come **SysAllocStringLen**, che include un parametro esplicito per la lunghezza:


```C++
BSTR filter = SysAllocStringLen(L"Video\0*.avi\0", 12);
// Note: SysAllocStringLen appends an additional '\0' to the string.
```



Se l'utente annulla la finestra di dialogo Apri file, il metodo restituisce E \_ FAIL.

Il metodo alloca memoria per **BSTR** in *pOutput*. L'applicazione deve **chiamare SysFreeString** per liberare la memoria.

> [!Note]  
> Il file di intestazione Qedit.h non è compatibile con le intestazioni Direct3D successive alla versione 7.

 

> [!Note]  
> Per ottenere Qedit.h, scaricare l'aggiornamento di Microsoft Windows SDK per Windows [Vista e .NET Framework 3.0.](https://msdn.microsoft.com/windowsvista/bb980924.aspx) Qedit.h non è disponibile in Microsoft Windows SDK per Windows 7 e .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Libreria<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IMediaLocator**](imedialocator.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 
