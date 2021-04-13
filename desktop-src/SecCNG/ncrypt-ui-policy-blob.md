---
description: Utilizzato con la \_ proprietà della proprietà dei criteri dell'interfaccia utente NCRYPT \_ \_ per contenere informazioni sull'interfaccia utente per una chiave.
ms.assetid: c567d8ba-3315-4316-8e09-93b2c10a55ec
title: Struttura NCRYPT_UI_POLICY_BLOB ( \_ provider NCRYPT. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NCRYPT_UI_POLICY_BLOB
api_type:
- HeaderDef
api_location:
- Ncrypt_provider.h
ms.openlocfilehash: c45b53e051f021ab3dcce6dab4e2317572338624
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528728"
---
# <a name="ncrypt_ui_policy_blob-structure"></a>\_ \_ Struttura BLOB dei criteri dell'interfaccia utente di NCRYPT \_

La struttura del **\_ \_ \_ BLOB dei criteri** dell'interfaccia utente di NCRYPT viene usata con la proprietà della [**\_ \_ \_ proprietà dei criteri**](key-storage-property-identifiers.md) dell'interfaccia utente NCRYPT per contenere informazioni sull'interfaccia utente per una chiave.

## <a name="syntax"></a>Sintassi


```C++
typedef struct __NCRYPT_UI_POLICY_BLOB {
  DWORD dwVersion;
  DWORD dwFlags;
  DWORD cbCreationTitle;
  DWORD cbFriendlyName;
  DWORD cbDescription;
} NCRYPT_UI_POLICY_BLOB;
```



## <a name="members"></a>Members

<dl> <dt>

**dwVersion**
</dt> <dd>

Numero di versione della struttura. Questo membro deve contenere 1.

</dd> <dt>

**dwFlags**
</dt> <dd>

Set di flag che forniscono informazioni o requisiti aggiuntivi dell'interfaccia utente.



| Valore                                                                                                                                                                                                                                                                                                  | Significato                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <span id="NCRYPT_UI_PROTECT_KEY_FLAG"></span><span id="ncrypt_ui_protect_key_flag"></span><dl> <dt>**NCRYPT \_ \_ \_ \_ Flag chiave di protezione interfaccia utente**</dt> <dt>0x00000001</dt> </dl>                                | Visualizzare l'interfaccia utente chiave avanzata in base alle esigenze.<br/> |
| <span id="NCRYPT_UI_FORCE_HIGH_PROTECTION_FLAG"></span><span id="ncrypt_ui_force_high_protection_flag"></span><dl> <dt>**NCRYPT \_ Interfaccia utente-0x00000002 \_ \_ \_ \_ flag di protezione elevata**</dt> <dt></dt> </dl> | Forza la protezione elevata.<br/>                           |



 

</dd> <dt>

**cbCreationTitle**
</dt> <dd>

Lunghezza, in byte, del titolo di creazione. Il titolo della creazione è una stringa Unicode con terminazione null che specifica il testo usato come titolo della finestra di dialogo chiave complessa al termine della chiave. Il titolo di creazione deve essere inserito immediatamente dopo la struttura del **\_ \_ \_ BLOB dei criteri dell'interfaccia utente di NCRYPT** . Se il valore del membro **cbCreationTitle** è impostato su 0, per il titolo della finestra di dialogo chiave complessa viene utilizzato un titolo di creazione predefinito. Questo membro viene utilizzato solo alla finalizzazione della chiave.

</dd> <dt>

**cbFriendlyName**
</dt> <dd>

Lunghezza, in byte, del nome descrittivo della chiave. Il nome descrittivo è una stringa Unicode con terminazione null che contiene il testo visualizzato nella finestra di dialogo chiave complessa come nome della chiave. Il nome descrittivo deve essere inserito immediatamente dopo il titolo di creazione in questo BLOB. Se il valore del membro **cbFriendlyName** è impostato su 0, nella finestra di dialogo chiave complessa viene utilizzato un nome predefinito. Questo membro viene utilizzato sia quando la chiave viene completata sia quando viene utilizzata la chiave.

</dd> <dt>

**cbDescription**
</dt> <dd>

Lunghezza, in byte, della descrizione della chiave. La descrizione della chiave è una stringa Unicode con terminazione null che contiene il testo visualizzato nella finestra di dialogo chiave complessa come descrizione della chiave. Il valore della descrizione deve essere inserito immediatamente dopo il nome descrittivo in questo BLOB. Se il valore del membro **cbDescription** è impostato su 0, nella finestra di dialogo chiave complessa viene utilizzata una descrizione predefinita. Questo membro viene utilizzato sia quando la chiave viene completata sia quando viene utilizzata la chiave.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa struttura è inclusa nell'intestazione ncrypt \_ provider. h. Per utilizzare la struttura, è necessario scaricare [Cryptographic Provider Development Kit](/collaborate/connect-redirect?InvitationID=CSDK-GYTG-R2PX&ProgramID=7264) da Microsoft Connect.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                          |
| Intestazione<br/>                   | <dl> <dt>\_Provider ncrypt. h</dt> </dl> |



 

