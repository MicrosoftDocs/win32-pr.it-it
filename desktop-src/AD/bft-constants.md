---
title: Costanti BFT (Ntdsbcli.h)
description: Le costanti BFT vengono usate come flag di bit per identificare tipi di file diversi in un Active Directory Domain Services backup.
ms.assetid: 3658a657-d9e3-4fbf-9120-4b0205b81a36
ms.tgt_platform: multiple
topic_type:
- apiref
api_name:
- BFT_LOG_DIRECTORY
- BFT_DATABASE_DIRECTORY
- BFT_DIRECTORY
- BFT_LOG
- BFT_LOG_DIR
- BFT_CHECKPOINT_DIR
- BFT_NTDS_DATABASE
- BFT_PATCH_FILE
- BFT_UNKNOWN
api_location:
- Ntdsbcli.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b5e9275e01b8c33d308b55b2638d4eaf186b8f5265834acc27acd2f146f0d09
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118024050"
---
# <a name="bft-constants"></a>Costanti BFT

Le costanti BFT vengono usate come flag di bit per identificare tipi di file diversi in un Active Directory Domain Services backup.

<dl> <dt>

<span id="BFT_LOG_DIRECTORY"></span><span id="bft_log_directory"></span>**DIRECTORY DI LOG BFT \_ \_**
</dt> <dd> <dl> <dt>

0x20
</dt> <dt>



Il file appartiene alla directory di log.


</dt> </dl> </dd> <dt>

<span id="BFT_DATABASE_DIRECTORY"></span><span id="bft_database_directory"></span>**DIRECTORY \_ DEL DATABASE BFT \_**
</dt> <dd> <dl> <dt>

0x40
</dt> <dt>



Il file appartiene alla directory del database.


</dt> </dl> </dd> <dt>

<span id="BFT_DIRECTORY"></span><span id="bft_directory"></span>**BFT \_ DIRECTORY**
</dt> <dd> <dl> <dt>

0x80
</dt> <dt>



Il percorso specificato è una directory e non un nome file.


</dt> </dl> </dd> <dt>

<span id="BFT_LOG"></span><span id="bft_log"></span>**BFT \_ LOG**
</dt> <dd> <dl> <dt>

0x21
</dt> <dt>



Specifica un file di log che appartiene alla directory di log.


</dt> </dl> </dd> <dt>

<span id="BFT_LOG_DIR"></span><span id="bft_log_dir"></span>**BFT \_ LOG \_ DIR**
</dt> <dd> <dl> <dt>

0x22
</dt> <dt>



Il file è il percorso della directory di log.


</dt> </dl> </dd> <dt>

<span id="BFT_CHECKPOINT_DIR"></span><span id="bft_checkpoint_dir"></span>**BFT \_ CHECKPOINT \_ DIR**
</dt> <dd> <dl> <dt>

0x23
</dt> <dt>



Il file è il percorso della directory del checkpoint.


</dt> </dl> </dd> <dt>

<span id="BFT_NTDS_DATABASE"></span><span id="bft_ntds_database"></span>**BFT \_ NTDS \_ DATABASE**
</dt> <dd> <dl> <dt>

0x44
</dt> <dt>



Il file è un database del servizio directory che appartiene alla directory del database.


</dt> </dl> </dd> <dt>

<span id="BFT_PATCH_FILE"></span><span id="bft_patch_file"></span>**BFT \_ PATCH \_ FILE**
</dt> <dd> <dl> <dt>

0x25
</dt> <dt>



Il file è un file di patch che appartiene alla directory di log.


</dt> </dl> </dd> <dt>

<span id="BFT_UNKNOWN"></span><span id="bft_unknown"></span>**BFT \_ UNKNOWN**
</dt> <dd> <dl> <dt>

0x0F
</dt> <dt>



Il file non può essere riconosciuto. Il file non coincide con i nomi e i tipi di file noti.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                              |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                        |
| Intestazione<br/>                   | <dl> <dt>Ntdsbcli.h</dt> </dl> |



 

 





