---
title: CB_DIR messaggio (Winuser.h)
description: Aggiunge nomi all'elenco visualizzato dalla casella combinata. Il messaggio aggiunge i nomi delle directory e dei file che corrispondono a una stringa e a un set di attributi di file specificati. CB \_ DIR può anche aggiungere lettere di unità mappate all'elenco.
ms.assetid: 6082d12c-0af4-4a99-98c0-6a98d171f4d8
keywords:
- CB_DIR controlli Windows messaggio
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
ms.openlocfilehash: defa19ffdebfb448e1a89c141da0b275c1df1bffdcfa9e3914293400d706b7ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119577121"
---
# <a name="cb_dir-message"></a>CB \_ DIR message (Messaggio DIR CB)

Aggiunge nomi all'elenco visualizzato dalla casella combinata. Il messaggio aggiunge i nomi delle directory e dei file che corrispondono a una stringa e a un set di attributi di file specificati. **CB \_ DIR** può anche aggiungere lettere di unità mappate all'elenco.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Attributi dei file o delle directory da aggiungere alla casella combinata. Questo parametro può essere uno o più dei valori seguenti.



| Valore                                                                                                                                                         | Significato                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DDL_ARCHIVE"></span><span id="ddl_archive"></span><dl> <dt>**ARCHIVIO \_ DDL**</dt> </dl>       | Include i file archiviati.<br/>                                                                                                            |
| <span id="DDL_DIRECTORY"></span><span id="ddl_directory"></span><dl> <dt>**DDL \_ DIRECTORY**</dt> </dl> | Include le sottodirectory, racchiuse tra parentesi quadre ( \[ \] ).<br/>                                                             |
| <span id="DDL_DRIVES"></span><span id="ddl_drives"></span><dl> <dt>**UNITÀ \_ DDL**</dt> </dl>          | Tutte le unità mappate vengono aggiunte all'elenco. Le unità sono elencate nel formato \[ - *x* - \] , dove *x* è la lettera di unità.<br/>                    |
| <span id="DDL_EXCLUSIVE"></span><span id="ddl_exclusive"></span><dl> <dt>**DDL \_ EXCLUSIVE**</dt> </dl> | Include solo i file con gli attributi specificati. Per impostazione predefinita, i file di lettura/scrittura vengono elencati anche se non è specificato DDL \_ READWRITE.<br/> |
| <span id="DDL_HIDDEN"></span><span id="ddl_hidden"></span><dl> <dt>**DDL \_ HIDDEN**</dt> </dl>          | Include i file nascosti.<br/>                                                                                                              |
| <span id="DDL_READONLY"></span><span id="ddl_readonly"></span><dl> <dt>**DDL \_ READONLY**</dt> </dl>    | Include file di sola lettura.<br/>                                                                                                           |
| <span id="DDL_READWRITE"></span><span id="ddl_readwrite"></span><dl> <dt>**DDL \_ READWRITE**</dt> </dl> | Include file di lettura/scrittura senza attributi aggiuntivi. Questo è il valore predefinito.<br/>                                                       |
| <span id="DDL_SYSTEM"></span><span id="ddl_system"></span><dl> <dt>**DDL \_ SYSTEM**</dt> </dl>          | Include i file di sistema.<br/>                                                                                                              |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore **LPCTSTR** a una stringa con terminazione Null che specifica un percorso assoluto, un percorso relativo o un nome file. Un percorso assoluto può iniziare con una lettera di unità (ad esempio, d: o un nome UNC, ad esempio \) \\ \\ *nomecomputer* \\ *nomecontenizione*). Se la stringa specifica un nome file o una directory con gli attributi specificati dal *parametro wParam,* il nome file o la directory viene aggiunto all'elenco. Se il nome file o il nome della directory contiene caratteri jolly (? o ), tutti i file o le directory che corrispondono all'espressione con caratteri jolly e hanno gli attributi specificati dal parametro wParam vengono aggiunti all'elenco \* visualizzato nella casella combinata. 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il messaggio ha esito positivo, il valore restituito è l'indice in base zero del cognome aggiunto all'elenco.

Se si verifica un errore, il valore restituito è CB \_ ERR. Se lo spazio disponibile non è sufficiente per archiviare le nuove stringhe, il valore restituito è CB \_ ERRSPACE.

## <a name="remarks"></a>Commenti

Se *wParam* include il flag DDL DIRECTORY e lParam specifica tutte le sottodirectory di una directory di primo livello, ad esempio C: TEMP , la casella di riepilogo includerà sempre una voce \_  \\ \\ \* ".." per la directory radice. Questo vale anche se la directory radice ha attributi di sistema o nascosti e i flag DDL HIDDEN e \_ DDL \_ SYSTEM non sono specificati. La directory radice di un volume NTFS contiene attributi di sistema e nascosti.

L'elenco visualizza i nomi file lunghi, se presenti.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



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

 

 





