---
description: Il metodo Directory recupera un elenco di file del tipo specificato dalla directory corrente.
ms.assetid: 0ae89811-7534-497b-af9f-ae37a48bc3e5
title: Metodo ISCardFileAccess::D irectory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.Directory
api_type:
- COM
api_location: ''
ms.openlocfilehash: 009263a92f014367636c7ff16b7f43635f73fa1b2ed17b52d53e81152c6e15b6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119481301"
---
# <a name="iscardfileaccessdirectory-method"></a>Metodo ISCardFileAccess::D irectory

\[Il **metodo Directory** è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. Non è disponibile per l'uso in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. I [moduli smart card offrono](/previous-versions/windows/desktop/secsmart/smart-card-modules) funzionalità simili.\]

Il **metodo Directory** recupera un elenco di file del tipo specificato dalla directory corrente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Directory(
  [in]  FILETYPE    fileType,
  [out] LPSAFEARRAY *ppFileList
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*tipo di file* \[ Pollici\]
</dt> <dd>

Tipo di [*smart card*](../secgloss/s-gly.md) file da elencare.



| Valore                                                                                                                                                                                      | Significato                                              |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <span id="SC_TYPE_DIRECTORIES"></span><span id="sc_type_directories"></span><dl> <dt>**DIRECTORY \_ DEI TIPI \_ SC**</dt> </dl>           | Elencare solo i file di directory.<br/>                |
| <span id="SC_TYPE_FILES"></span><span id="sc_type_files"></span><dl> <dt>**FILE \_ DI TIPO \_ SC**</dt> </dl>                             | Elencare solo i file elementari.<br/>               |
| <span id="SC_TYPE_ALL_FILES"></span><span id="sc_type_all_files"></span><dl> <dt>**SC \_ DIGITARE TUTTI I \_ \_ FILE**</dt> </dl>                | Elencare sia i file di directory che i file elementari.<br/> |
| <span id="SC_TYPE_DIRECTORY_FILE"></span><span id="sc_type_directory_file"></span><dl> <dt>**SC \_ TYPE \_ DIRECTORY \_ FILE**</dt> </dl> | File di directory.<br/>                           |
| <span id="SC_TYPE_TRANSPARENT_EF"></span><span id="sc_type_transparent_ef"></span><dl> <dt>**SC \_ TYPE \_ TRANSPARENT \_ EF**</dt> </dl> | File elementare trasparente.<br/>              |
| <span id="SC_TYPE_FIXED_EF"></span><span id="sc_type_fixed_ef"></span><dl> <dt>**SC \_ TYPE \_ FIXED \_ EF**</dt> </dl>                   | File elementare fisso lineare.<br/>             |
| <span id="SC_TYPE_CYCLIC_EF"></span><span id="sc_type_cyclic_ef"></span><dl> <dt>**SC \_ TYPE \_ CYCLIC \_ EF**</dt> </dl>                | File elementare ciclico.<br/>                   |
| <span id="SC_TYPE_VARIABLE_EF"></span><span id="sc_type_variable_ef"></span><dl> <dt>**SC \_ TYPE \_ VARIABLE \_ EF**</dt> </dl>          | File elementare di variabili lineari.<br/>          |



 

</dd> <dt>

*ppFileList* \[ Cambio\]
</dt> <dd>

Matrice di oggetti BSTR che rappresentano l'elenco di file corrispondenti all'identificatore in *fileType*.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce uno dei valori possibili seguenti.



| Codice restituito                                                                                   | Descrizione                                               |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | L'operazione è stata completata correttamente.<br/>          |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Parametro non valido.<br/>                             |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | L'interfaccia non ha implementato questo metodo.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insufficiente.<br/>                                 |
| <dl> <dt>**PUNTATORE \_ E**</dt> </dl>     | È stato passato un puntatore non valido per *ppFileList*.<br/>  |



 

## <a name="remarks"></a>Commenti

Per un elenco di tutti i metodi definiti da questa interfaccia, vedere [**ISCardFileAccess.**](iscardfileaccess.md)

Oltre ai codici di errore COM elencati in precedenza, questa interfaccia può restituire un codice di errore smart card se è stata chiamata una funzione smart card per completare la richiesta. Per altre informazioni, vedere [Valori restituiti delle smart card.](authentication-return-values.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>          |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/> |
| Fine del supporto client<br/>    | Windows XP<br/>                                |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ISCardFileAccess**](iscardfileaccess.md)
</dt> </dl>

 

 
