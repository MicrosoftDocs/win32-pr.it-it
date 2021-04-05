---
title: Messaggio CB_DIR (winuser. h)
description: Aggiunge nomi all'elenco visualizzato dalla casella combinata. Il messaggio aggiunge i nomi delle directory e dei file che corrispondono a una stringa specificata e a un set di attributi di file. \_Il dir dir può anche aggiungere lettere di unità mappate all'elenco.
ms.assetid: 6082d12c-0af4-4a99-98c0-6a98d171f4d8
keywords:
- Controlli di Windows Message CB_DIR
topic_type:
- apiref
api_name:
- CB_DIR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98cbea5bb88614d5606dd3d5cb165be59f632556
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873805"
---
# <a name="cb_dir-message"></a>\_Messaggio dir CB

Aggiunge nomi all'elenco visualizzato dalla casella combinata. Il messaggio aggiunge i nomi delle directory e dei file che corrispondono a una stringa specificata e a un set di attributi di file. **CB \_ DIR** può anche aggiungere lettere di unità mappate all'elenco.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Attributi dei file o delle directory da aggiungere alla casella combinata. Il parametro può essere costituito da uno o più dei valori seguenti.



| Valore                                                                                                                                                         | Significato                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DDL_ARCHIVE"></span><span id="ddl_archive"></span><dl> <dt>**\_Archivio DDL**</dt> </dl>       | Include i file archiviati.<br/>                                                                                                            |
| <span id="DDL_DIRECTORY"></span><span id="ddl_directory"></span><dl> <dt>**\_directory DDL**</dt> </dl> | Include le sottodirectory, racchiuse tra parentesi quadre ( \[ \] ).<br/>                                                             |
| <span id="DDL_DRIVES"></span><span id="ddl_drives"></span><dl> <dt>**\_unità DDL**</dt> </dl>          | Tutte le unità mappate vengono aggiunte all'elenco. Le unità sono elencate nel formato \[ - *x* - \] , dove *x* è la lettera di unità.<br/>                    |
| <span id="DDL_EXCLUSIVE"></span><span id="ddl_exclusive"></span><dl> <dt>**\_esclusiva DDL**</dt> </dl> | Include solo i file con gli attributi specificati. Per impostazione predefinita, i file di lettura/scrittura sono elencati anche se DDL \_ ReadWrite non è specificato.<br/> |
| <span id="DDL_HIDDEN"></span><span id="ddl_hidden"></span><dl> <dt>**DDL \_ nascosto**</dt> </dl>          | Include i file nascosti.<br/>                                                                                                              |
| <span id="DDL_READONLY"></span><span id="ddl_readonly"></span><dl> <dt>**sola \_ lettura DDL**</dt> </dl>    | Include i file di sola lettura.<br/>                                                                                                           |
| <span id="DDL_READWRITE"></span><span id="ddl_readwrite"></span><dl> <dt>**\_ReadWrite DDL**</dt> </dl> | Include i file di lettura/scrittura senza attributi aggiuntivi. Questo è il valore predefinito.<br/>                                                       |
| <span id="DDL_SYSTEM"></span><span id="ddl_system"></span><dl> <dt>**\_sistema DDL**</dt> </dl>          | Include i file di sistema.<br/>                                                                                                              |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore **LPCTSTR** a una stringa con terminazione null che specifica un percorso assoluto, un percorso relativo o un nome file. Un percorso assoluto può iniziare con una lettera di unità (ad esempio, d: \) o un nome UNC, ad esempio \\ \\ *machineName* \\ *ShareName*). Se la stringa specifica un nome file o una directory con gli attributi specificati dal parametro *wParam* , il nome file o la directory viene aggiunta all'elenco. Se il nome file o il nome della directory contiene caratteri jolly (? o \* ), tutti i file o le directory che corrispondono all'espressione con caratteri jolly e che hanno gli attributi specificati dal parametro *wParam* vengono aggiunti all'elenco visualizzato nella casella combinata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il messaggio ha esito positivo, il valore restituito è l'indice in base zero del cognome aggiunto all'elenco.

Se si verifica un errore, il valore restituito è CB \_ Err. Se non è disponibile spazio sufficiente per archiviare le nuove stringhe, il valore restituito è CB \_ ERRSPACE.

## <a name="remarks"></a>Commenti

Se *wParam* include il \_ flag di directory DDL e *lParam* specifica tutte le sottodirectory di una directory di primo livello, ad esempio C: \\ temp \\ \* , nella casella di riepilogo viene sempre inclusa una voce ".." per la directory radice. Questo vale anche se la directory radice contiene attributi di sistema o nascosti e i \_ flag DDL Hidden e DDL \_ System non sono specificati. La directory radice di un volume NTFS presenta gli attributi nascosti e di sistema.

L'elenco Visualizza i nomi di file lunghi, se presenti.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**CB \_ ADDSTRING**](cb-addstring.md)
</dt> <dt>

[**CB \_ INSERTSTRING**](cb-insertstring.md)
</dt> <dt>

[**DlgDirListComboBox**](/windows/desktop/api/Winuser/nf-winuser-dlgdirlistcomboboxa)
</dt> </dl>

 

 





