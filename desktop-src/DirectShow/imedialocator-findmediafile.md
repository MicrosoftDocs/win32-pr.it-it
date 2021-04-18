---
description: Il metodo FindMediaFile Cerca un file e, in caso di esito positivo, recupera il percorso del file.
ms.assetid: ddfa2c75-e51f-4aad-afe6-8a60c46e8d35
title: 'Metodo IMediaLocator:: FindMediaFile (qedit. h)'
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
ms.openlocfilehash: 3561b77873c90b2d4bd0202bed8e2da822a0362f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325300"
---
# <a name="imedialocatorfindmediafile-method"></a>Metodo IMediaLocator:: FindMediaFile

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `FindMediaFile` metodo cerca un file e, in caso di esito positivo, recupera il percorso del file.

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

Nome del file, incluso il percorso, in cui si trovava l'ultima versione del file. Per gli oggetti di origine nella sequenza temporale, usare il nome del supporto corrente.

</dd> <dt>

*FilterString* 
</dt> <dd>

**BSTR** contenente coppie di stringhe di filtro, formattate come richiesto dal membro **LpstrFilter** della struttura [**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) . Il localizzatore multimediale usa questo filtro se Visualizza una finestra di dialogo Apri file. Il valore può essere **null** se il parametro *Flags* non include il \_ \_ flag popup SFN VALIDATEF.

</dd> <dt>

*pOutput* 
</dt> <dd>

Puntatore a una variabile che riceve il percorso effettivo del file, se è diverso dal valore contenuto nell' *input* e se il metodo individua correttamente il file.

</dd> <dt>

*Flag* 
</dt> <dd>

Combinazione bit per bit di zero o più flag. Per un elenco di flag possibili, vedere [**flag di convalida dei nomi di file**](file-name-validation-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

La stringa di filtro per la finestra di dialogo Apri file, specificata dal parametro *FilterString* , contiene caratteri null interni. Ad esempio, \\ il video 0 \* . avi \\ 0 \\ 0 è una stringa di filtro valida. Non è possibile usare la funzione **SysAllocStr** per allocare BSTR, perché tale funzione prevede una stringa con terminazione null e tronca la stringa in corrispondenza del primo carattere null. Utilizzare pertanto una funzione come **SysAllocStringLen**, che include un parametro esplicito per la lunghezza:


```C++
BSTR filter = SysAllocStringLen(L"Video\0*.avi\0", 12);
// Note: SysAllocStringLen appends an additional '\0' to the string.
```



Se l'utente annulla la finestra di dialogo Apri file, il metodo restituisce E ha \_ esito negativo.

Il metodo alloca memoria per **BSTR** in *pOutput*. Per liberare la memoria, l'applicazione deve chiamare **SysFreeString** .

> [!Note]  
> Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.

 

> [!Note]  
> Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Qedit. h</dt> </dl>      |
| Libreria<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IMediaLocator**](imedialocator.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 
