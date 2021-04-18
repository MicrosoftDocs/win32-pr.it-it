---
description: Contiene informazioni sulla finestra di dialogo visualizzata dalla funzione CryptUIDlgSelectCertificate.
ms.assetid: 073a67a0-427b-4b81-82a0-1bb0a216a335
title: Struttura CRYPTUI_SELECTCERTIFICATE_STRUCT
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRYPTUI_SELECTCERTIFICATE_STRUCT
- CRYPTUI_SELECTCERTIFICATE_STRUCTA
- CRYPTUI_SELECTCERTIFICATE_STRUCTW
api_type:
- NA
api_location: ''
ms.openlocfilehash: 3db7e59006e964b7335a4a246fb63d7ca7b80577
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318247"
---
# <a name="cryptui_selectcertificate_struct-structure"></a>\_ \_ Struttura struct SELECTCERTIFICATE CRYPTUI

La struttura **CRYPTUI \_ SELECTCERTIFICATE \_ struct** contiene informazioni sulla finestra di dialogo visualizzata dalla funzione [**CryptUIDlgSelectCertificate**](cryptuidlgselectcertificate.md) .

## <a name="syntax"></a>Sintassi


```C++
typedef struct _CRYPTUI_SELECTCERTIFICATE_STRUCT {
  DWORD               dwSize;
  HWND                hwndParent;
  DWORD               dwFlags;
  LPCTSTR             szTitle;
  DWORD               dwDontUseColumn;
  LPCTSTR             szDisplayString;
  PFNCFILTERPROC      pFilterCallback;
  PFNCCERTDISPLAYPROC pDisplayCallback;
  void                *pvCallbackData;
  DWORD               cDisplayStores;
  HCERTSTORE          *rghDisplayStores;
  DWORD               cStores;
  HCERTSTORE          *rghStores;
  DWORD               cPropSheetPages;
  LPCPROPSHEETPAGE    rgPropSheetPages;
  HCERTSTORE          hSelectedCertStore;
} CRYPTUI_SELECTCERTIFICATE_STRUCT, *PCRYPTUI_SELECTCERTIFICATE_STRUCT;
```



## <a name="members"></a>Members

<dl> <dt>

**dwSize**
</dt> <dd>

Dimensione, in byte, della struttura.

</dd> <dt>

**hwndParent**
</dt> <dd>

Handle della finestra padre della finestra di dialogo. Se questo valore è **null**, la finestra padre è la finestra desktop predefinita.

</dd> <dt>

**dwFlags**
</dt> <dd>

Specifica opzioni aggiuntive per la funzione [**CryptUIDlgSelectCertificate**](cryptuidlgselectcertificate.md) . Può essere zero o un **or** bit per bit dei valori seguenti.



| Valore                                                                                                                                                                                                                                    | Significato                                                                                                                                                                                                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CRYPTUI_SELECTCERT_ADDFROMDS"></span><span id="cryptui_selectcert_addfromds"></span><dl> <dt>**CRYPTUI \_ SELECTCERT \_ ADDFROMDS**</dt> </dl>                              | Riservato.<br/>                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="CRYPTUI_SELECTCERT_LEGACY"></span><span id="cryptui_selectcert_legacy"></span><dl> <dt>**CRYPTUI \_ SELECTCERT \_ legacy**</dt> </dl>                                       | Specifica che deve essere visualizzata la finestra di dialogo legacy.<br/>                                                                                                                                                                                                                                                                                                                      |
| <span id="CRYPTUI_SELECTCERT_MULTISELECT"></span><span id="cryptui_selectcert_multiselect"></span><dl> <dt>**CRYPTUI \_ SELECTCERT \_ MultiSelect**</dt> </dl>                        | Consente all'utente di selezionare più di un certificato nella finestra di dialogo. Se questo flag è impostato, la funzione [**CryptUIDlgSelectCertificate**](cryptuidlgselectcertificate.md) restituisce sempre **null**. Il membro **hSelectedCertStore** di questa struttura deve contenere un handle per un archivio certificati. I certificati selezionati dall'utente verranno aggiunti a questo archivio.<br/> |
| <span id="CRYPTUI_SELECTCERT_PUT_WINDOW_TOPMOST"></span><span id="cryptui_selectcert_put_window_topmost"></span><dl> <dt>**CRYPTUI \_ SELECTCERT- \_ Inserisci \_ finestra \_ in primo piano**</dt> </dl> | Impone che l'interfaccia utente di crittografia sia la finestra superiore sullo schermo.<br/>                                                                                                                                                                                                                                                                                                            |



 

</dd> <dt>

**szTitle**
</dt> <dd>

Titolo visualizzato per la finestra di dialogo. Se il valore di questo membro è **null**, viene usato il titolo predefinito "Select certificate".

</dd> <dt>

**dwDontUseColumn**
</dt> <dd>

Flag che possono essere combinati per escludere le colonne della visualizzazione.



| Valore                                                                                                                                                                                                                                                                                       | Significato                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span id="CRYPTUI_SELECT_ISSUEDTO_COLUMN"></span><span id="cryptui_select_issuedto_column"></span><dl> <dt>**CRYPTUI \_ Selezionare \_ la \_ colonna ISSUEDTO**</dt> <dt>1 (0x1)</dt> </dl>             | Non visualizzare le informazioni **ISSUEDTO** .<br/>    |
| <span id="CRYPTUI_SELECT_ISSUEDBY_COLUMN"></span><span id="cryptui_select_issuedby_column"></span><dl> <dt>**CRYPTUI \_ Selezionare \_ la \_ colonna ISSUEDBY**</dt> <dt>2 (0x2)</dt> </dl>             | Non visualizzare le informazioni **ISSUEDBY** .<br/>    |
| <span id="CRYPTUI_SELECT_INTENDEDUSE_COLUMN"></span><span id="cryptui_select_intendeduse_column"></span><dl> <dt>**CRYPTUI \_ Seleziona \_ INTENDEDUSE \_ colonna**</dt> <dt>4 (0x4)</dt> </dl>    | Non visualizzare le informazioni **IntendedUse** .<br/> |
| <span id="CRYPTUI_SELECT_FRIENDLYNAME_COLUMN"></span><span id="cryptui_select_friendlyname_column"></span><dl> <dt>**CRYPTUI \_ Selezionare \_ FriendlyName \_ Column**</dt> <dt>8 (0x8)</dt> </dl> | Non visualizzare le informazioni sul nome.<br/>            |
| <span id="CRYPTUI_SELECT_LOCATION_COLUMN"></span><span id="cryptui_select_location_column"></span><dl> <dt>**CRYPTUI \_ Selezionare \_ la \_ colonna location**</dt> <dt>16 (0x10)</dt> </dl>           | Non visualizzare le informazioni sulla posizione.<br/>        |
| <span id="CRYPTUI_SELECT_EXPIRATION_COLUMN"></span><span id="cryptui_select_expiration_column"></span><dl> <dt>**CRYPTUI \_ Selezionare \_ la \_ colonna di scadenza**</dt> <dt>32 (0x20)</dt> </dl>     | Non visualizzare le informazioni sulla scadenza.<br/>      |



 

</dd> <dt>

**szDisplayString**
</dt> <dd>

Testo visualizzato nella finestra di dialogo per indicare all'utente. Se il valore di questo membro è **null**, viene usata la stringa predefinita "selezionare un certificato che si vuole usare".

</dd> <dt>

**pFilterCallback**
</dt> <dd>

Puntatore a una funzione di callback [**PFNCFILTERPROC**](/windows/desktop/api/Cryptuiapi/nc-cryptuiapi-pfncfilterproc) che filtra i certificati visualizzati nella finestra di dialogo.

</dd> <dt>

**pDisplayCallback**
</dt> <dd>

Puntatore a una funzione di callback [**PFNCCERTDISPLAYPROC**](pfnccertdisplayproc.md) che Visualizza i certificati selezionati dall'utente per la visualizzazione.

</dd> <dt>

**pvCallbackData**
</dt> <dd>

Dati aggiuntivi passati alle funzioni di callback specificate dai membri **pFilterCallback** e **pDisplayCallback** .

</dd> <dt>

**cDisplayStores**
</dt> <dd>

Numero di archivi certificati nella matrice **rghDisplayStores** .

</dd> <dt>

**rghDisplayStores**
</dt> <dd>

Puntatore a una matrice di archivi che contengono certificati disponibili per la selezione nella finestra di dialogo.

</dd> <dt>

**cStores**
</dt> <dd>

Numero di archivi certificati nella matrice **rghStores** .

</dd> <dt>

**rghStores**
</dt> <dd>

Puntatore a una matrice di archivi certificati da cercare durante la compilazione di una catena di certificati e la verifica dell'attendibilità per i certificati visualizzati nella finestra di dialogo.

</dd> <dt>

**cPropSheetPages**
</dt> <dd>

Numero di pagine delle proprietà nella matrice **rgPropSheetPages** .

</dd> <dt>

**rgPropSheetPages**
</dt> <dd>

Puntatore a una matrice di strutture **PROPSHEETPAGE** che rappresentano le pagine di proprietà passate alla finestra di dialogo visualizzazione certificati quando viene selezionato un certificato per la visualizzazione.

</dd> <dt>

**hSelectedCertStore**
</dt> <dd>

Handle per un archivio certificati creato dal chiamante. I certificati selezionati dall'utente vengono aggiunti a questo archivio. Se il numero di certificati in questo archivio è uguale prima e dopo la chiamata di [**CryptUIDlgSelectCertificate**](cryptuidlgselectcertificate.md), l'utente ha chiuso la finestra di dialogo senza selezionare alcun certificato.

Questo membro non viene utilizzato se il membro **dwFlags** di questa struttura non contiene il flag **CRYPTUI \_ SELECTCERT \_ MultiSelect** .

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                                                     |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                            |
| Nomi Unicode e ANSI<br/>   | **CRYPTUI \_ SELECTCERTIFICATE \_ STRUCTW** (Unicode) e **CRYPTUI \_ SELECTCERTIFICATE \_ STRUCTA** (ANSI)<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CryptUIDlgSelectCertificate**](cryptuidlgselectcertificate.md)
</dt> </dl>

 

 




