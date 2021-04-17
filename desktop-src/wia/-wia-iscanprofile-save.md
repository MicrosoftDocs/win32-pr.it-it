---
description: Salva le modifiche apportate a un profilo su disco.
ms.assetid: e844bd4c-93c3-44a3-b7d5-0beb71c9fa17
title: 'Metodo IScanProfile:: Save (scanprofile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.Save
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: 6d4787380344a7bf8adb70f4cb5a3eaacdea403a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527085"
---
# <a name="iscanprofilesave-method"></a>Metodo IScanProfile:: Save

Salva le modifiche apportate a un profilo su disco.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Save();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

Un profilo di analisi salvato è un file XML archiviato in% USERPROFILE% \\ dati applicazione \\ Microsoft \\ Document Center \\ UserScanProfiles.

Se più di un processo scrive nell'oggetto [**IScanProfile**](-wia-iscanprofile.md) , quello che chiama **IScanProfile:: Save** Last è l'unico processo le cui modifiche vengono salvate.

Il metodo **IScanProfile:: Save** convalida il profilo prima del salvataggio. Il profilo è sempre considerato valido a meno che la categoria dell'elemento Windows Image Acquisition (WIA) 2,0 associato al profilo sia WIA Category piano \_ \_ o WIA \_ Category \_ feeder. Se la categoria è la categoria WIA piano \_ \_ o \_ il \_ feeder di categoria WIA, le proprietà seguenti devono essere valide per l'elemento, se le proprietà sono contenute nel profilo:

\_luminosità IP \_ WIA

\_contrasto indirizzi IP WIA \_

tipo di dati \_ IPA WIA \_

\_indirizzi IP WIA \_ XRES

\_formato ipa \_ WIA

Se, inoltre, la categoria è il \_ feeder di categoria WIA \_ , la \_ proprietà delle dimensioni di pagina degli indirizzi IP WIA \_ \_ deve essere valida, se presente nel profilo. Per ulteriori informazioni su queste proprietà, vedere la pagina relativa alle [**costanti della proprietà Item di scanner WIA**](-wia-wiaitempropscanneritem.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                              |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                        |
| Intestazione<br/>                   | <dl> <dt>Scanprofile. h</dt> </dl>    |
| IDL<br/>                      | <dl> <dt>Scanprofiles. idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IScanProfile**](-wia-iscanprofile.md)
</dt> <dt>

[Schema del profilo di analisi](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




