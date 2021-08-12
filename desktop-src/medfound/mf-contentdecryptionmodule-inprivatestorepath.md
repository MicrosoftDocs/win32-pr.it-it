---
description: Specifica un percorso di file che rappresenta una posizione di archiviazione che il modulo di decrittografia di contenuto (CDM) può usare per i dati specifici del contenuto.
title: MF_CONTENTDECRYPTIONMODULE_INPRIVATESTOREPATH (mfcontentdecryptionmodule.h)
ms.topic: reference
ms.date: 01/31/2020
ms.openlocfilehash: bf03d4411ac2959a336b931bc5e45ec969772ab35c194de03cbd9c74aaca0c0c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118244774"
---
# <a name="mf_contentdecryptionmodule_inprivatestorepath-property"></a>MF \_ CONTENTDECRYPTIONMODULE \_ - proprietà INPRIVATESTOREPATH

Specifica un percorso di file che rappresenta una posizione di archiviazione che il modulo di decrittografia di contenuto (CDM) può usare per i dati specifici del contenuto.


## <a name="data-type"></a>Tipo di dati

**LPWSTR** (VT_LPWSTR)

## <a name="property-guid"></a>GUID proprietà

**MF \_ CONTENTDECRYPTIONMODULE \_ INPRIVATESTOREPATH**

## <a name="property-value"></a>Valore proprietà

Percorso di file che rappresenta una posizione di archiviazione che il modulo di decrittografia di contenuto (CDM) può usare per i dati specifici del contenuto.

## <a name="remarks"></a>Commenti

L'app deve eliminare la posizione dello Store dopo il rilascio dell'oggetto CDM.

Se questa proprietà non è impostata, il sistema userà il percorso specificato con la [proprietà MF_CONTENTDECRYPTIONMODULE_STOREPATH](mf-contentdecryptionmodule-storepath.md) per i dati specifici del contenuto.

Impostare questa proprietà quando si crea un cdm chiamando [IMFContentDecryptionModuleAccess::CreateContentDecryptionModule](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmoduleaccess-createcontentdecryptionmodule).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 10 Aggiornamento di aprile 2020<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>mfcontentdecryptionmodule.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

- [Media Foundation proprietà](media-foundation-properties.md)
- [IMFContentDecryptionModuleAccess::CreateContentDecryptionModule](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmoduleaccess-createcontentdecryptionmodule)


 

 




