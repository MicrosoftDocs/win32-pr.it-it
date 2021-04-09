---
title: Messaggio LB_DIR (winuser. h)
description: Aggiunge nomi all'elenco visualizzato da una casella di riepilogo. Il messaggio aggiunge i nomi delle directory e dei file che corrispondono a una stringa specificata e a un set di attributi di file. LB \_ dir può anche aggiungere lettere di unità mappate alla casella di riepilogo.
ms.assetid: 5ec134e9-fe42-4cc0-bdea-fa5e66c218f6
keywords:
- Controlli di Windows Message LB_DIR
topic_type:
- apiref
api_name:
- LB_DIR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80abddbce13adec2e66824057fc5e873def306ad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121318"
---
# <a name="lb_dir-message"></a>\_Messaggio dir lb

Aggiunge nomi all'elenco visualizzato da una casella di riepilogo. Il messaggio aggiunge i nomi delle directory e dei file che corrispondono a una stringa specificata e a un set di attributi di file. **Lb \_ DIR** può anche aggiungere lettere di unità mappate alla casella di riepilogo.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Attributi dei file o delle directory da aggiungere alla casella di riepilogo. Il parametro può essere costituito da uno o più dei valori seguenti.



| Valore                                                                                                                                                         | Significato                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DDL_ARCHIVE"></span><span id="ddl_archive"></span><dl> <dt>**\_Archivio DDL**</dt> </dl>       | Include i file archiviati.<br/>                                                                                                            |
| <span id="DDL_DIRECTORY"></span><span id="ddl_directory"></span><dl> <dt>**\_directory DDL**</dt> </dl> | Include le sottodirectory. I nomi delle sottodirectory sono racchiusi tra parentesi quadre ( \[ \] ).<br/>                                                |
| <span id="DDL_DRIVES"></span><span id="ddl_drives"></span><dl> <dt>**\_unità DDL**</dt> </dl>          | Tutte le unità mappate vengono aggiunte all'elenco. Le unità sono elencate nel formato \[ - *x* - \] , dove *x* è la lettera di unità.<br/>                    |
| <span id="DDL_EXCLUSIVE"></span><span id="ddl_exclusive"></span><dl> <dt>**\_esclusiva DDL**</dt> </dl> | Include solo i file con gli attributi specificati. Per impostazione predefinita, i file di lettura/scrittura sono elencati anche se DDL \_ ReadWrite non è specificato.<br/> |
| <span id="DDL_HIDDEN"></span><span id="ddl_hidden"></span><dl> <dt>**DDL \_ nascosto**</dt> </dl>          | Include i file nascosti.<br/>                                                                                                              |
| <span id="DDL_READONLY"></span><span id="ddl_readonly"></span><dl> <dt>**sola \_ lettura DDL**</dt> </dl>    | Include i file di sola lettura.<br/>                                                                                                           |
| <span id="DDL_READWRITE"></span><span id="ddl_readwrite"></span><dl> <dt>**\_ReadWrite DDL**</dt> </dl> | Include i file di lettura/scrittura senza attributi aggiuntivi. Si tratta dell'impostazione predefinita.<br/>                                               |
| <span id="DDL_SYSTEM"></span><span id="ddl_system"></span><dl> <dt>**\_sistema DDL**</dt> </dl>          | Include i file di sistema.<br/>                                                                                                              |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore alla stringa con terminazione null che specifica un percorso assoluto, un percorso relativo o un nome di file. Un percorso assoluto può iniziare con una lettera di unità (ad esempio, d: \) o un nome UNC, ad esempio \\ \\ *machineName* \\ *ShareName*).

Se la stringa specifica un nome file o una directory con gli attributi specificati dal parametro *wParam* , il nome file o la directory viene aggiunta all'elenco. Se il nome del file o della directory contiene caratteri jolly (? o \* ), all'elenco vengono aggiunti tutti i file o le directory che corrispondono all'espressione con caratteri jolly e che hanno gli attributi specificati dal parametro *wParam* .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il messaggio ha esito positivo, il valore restituito è l'indice in base zero del cognome aggiunto all'elenco.

Se si verifica un errore, il valore restituito è LB \_ Err. Se non è disponibile spazio sufficiente per archiviare le nuove stringhe, il valore restituito è LB \_ ERRSPACE.

## <a name="remarks"></a>Commenti

Il messaggio [**lb \_ INITSTORAGE**](lb-initstorage.md) consente di velocizzare l'inizializzazione di caselle di riepilogo con un numero elevato di elementi (più di 100). Si riserva la quantità di memoria specificata in modo che i messaggi di **lb \_ dir** successivi prendano il minor tempo possibile. È possibile utilizzare le stime per i parametri *wParam* e *lParam* . Se si esegue la sovrastima, viene allocata la memoria aggiuntiva. Se si sottovaluta, l'allocazione normale viene utilizzata per gli elementi che superano la quantità richiesta.

Se *wParam* include il \_ flag di directory DDL e *lParam* specifica tutte le sottodirectory di una directory di primo livello, ad esempio C: \\ temp \\ \* , nella casella di riepilogo viene sempre inclusa una voce ".." per la directory radice. Questo vale anche se la directory radice contiene attributi di sistema o nascosti e i \_ flag DDL Hidden e DDL \_ System non sono specificati. La directory radice di un volume NTFS presenta gli attributi nascosti e di sistema.

L'elenco Visualizza i nomi di file lunghi, se presenti.

Per un'applicazione ANSI, il sistema converte il testo in una casella di riepilogo in formato Unicode usando CP \_ ACP. Ciò può causare problemi. Ad esempio, i caratteri romani accentati in una casella di riepilogo non Unicode nelle finestre giapponesi verranno disattivati. Per risolvere questo problema, compilare l'applicazione come Unicode o utilizzare una casella di riepilogo creata dal proprietario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**DlgDirList**](/windows/desktop/api/Winuser/nf-winuser-dlgdirlista)
</dt> </dl>

 

 





