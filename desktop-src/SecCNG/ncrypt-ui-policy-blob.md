---
description: Usato con la proprietà NCRYPT \_ UI POLICY PROPERTY per \_ \_ contenere le informazioni sull'interfaccia utente per una chiave.
ms.assetid: c567d8ba-3315-4316-8e09-93b2c10a55ec
title: NCRYPT_UI_POLICY_BLOB struttura (provider \_ Ncrypt.h)
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
ms.openlocfilehash: 21f9f6c0f6956ffa89da45c9dcd23727c0b3cea2d4f31131713f9ed5a0c3a2fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118907601"
---
# <a name="ncrypt_ui_policy_blob-structure"></a>Struttura BLOB dei \_ criteri \_ dell'interfaccia utente NCRYPT \_

La **struttura BLOB dei criteri \_ \_ \_ dell'interfaccia** utente NCRYPT viene usata con la proprietà [**NCRYPT UI POLICY \_ \_ \_ PROPERTY**](key-storage-property-identifiers.md) per contenere le informazioni sull'interfaccia utente per una chiave.

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

Numero di versione della struttura . Questo membro deve contenere 1.

</dd> <dt>

**dwFlags**
</dt> <dd>

Set di flag che forniscono informazioni o requisiti aggiuntivi sull'interfaccia utente.



| Valore                                                                                                                                                                                                                                                                                                  | Significato                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <span id="NCRYPT_UI_PROTECT_KEY_FLAG"></span><span id="ncrypt_ui_protect_key_flag"></span><dl> <dt>**NCRYPT \_ FLAG \_ DELLA CHIAVE DI PROTEZIONE \_ \_ DELL'INTERFACCIA**</dt> <dt>0X00000001</dt> </dl>                                | Visualizzare l'interfaccia utente con chiave forte in base alle esigenze.<br/> |
| <span id="NCRYPT_UI_FORCE_HIGH_PROTECTION_FLAG"></span><span id="ncrypt_ui_force_high_protection_flag"></span><dl> <dt>**NCRYPT \_ FLAG \_ DI PROTEZIONE ELEVATA \_ \_ dell'interfaccia \_**</dt> <dt>utente</dt> 0X00000002 </dl> | Forzare la protezione elevata.<br/>                           |



 

</dd> <dt>

**cbCreationTitle**
</dt> <dd>

Lunghezza, in byte, del titolo di creazione. Il titolo di creazione è una stringa Unicode con terminazione Null che specifica il testo utilizzato come titolo della finestra di dialogo con chiave forte al termine della chiave. Il titolo di creazione deve essere posizionato immediatamente dopo la struttura BLOB **dei criteri \_ dell'interfaccia \_ utente \_ NCRYPT.** Se il valore del membro **cbCreationTitle** è impostato su 0, per il titolo della finestra di dialogo chiave forte viene usato un titolo di creazione predefinito. Questo membro viene usato solo per la finalizzazione della chiave.

</dd> <dt>

**cbFriendlyName**
</dt> <dd>

Lunghezza, in byte, del nome descrittivo della chiave. Il nome descrittivo è una stringa Unicode con terminazione Null che contiene il testo visualizzato nella finestra di dialogo chiave sicuro come nome della chiave. Il nome descrittivo deve essere inserito immediatamente dopo il titolo di creazione in questo BLOB. Se il valore del membro **cbFriendlyName** è impostato su 0, viene usato un nome predefinito nella finestra di dialogo chiave sicuro. Questo membro viene usato sia quando la chiave viene completata che quando viene usata la chiave.

</dd> <dt>

**cbDescription**
</dt> <dd>

Lunghezza, in byte, della descrizione della chiave. La descrizione della chiave è una stringa Unicode con terminazione Null che contiene il testo visualizzato nella finestra di dialogo chiave forte come descrizione della chiave. Il valore description deve essere inserito immediatamente dopo il nome descrittivo in questo BLOB. Se il valore del membro **cbDescription** è impostato su 0, nella finestra di dialogo chiave forte viene usata una descrizione predefinita. Questo membro viene usato sia quando la chiave viene completata che quando viene usata la chiave.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa struttura è inclusa nell'intestazione \_ Ncrypt provider.h. Per usare la struttura, è necessario scaricare [Cryptographic Provider Development Kit](/collaborate/connect-redirect?InvitationID=CSDK-GYTG-R2PX&ProgramID=7264) da Microsoft Connessione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                                |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                          |
| Intestazione<br/>                   | <dl> <dt>Provider \_ Ncrypt.h</dt> </dl> |



 

