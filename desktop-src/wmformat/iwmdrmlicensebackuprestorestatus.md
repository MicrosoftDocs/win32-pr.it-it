---
title: Interfaccia IWMDRMLicenseBackupRestoreStatus
description: L'interfaccia IWMDRMLicenseBackupRestoreStatus fornisce un metodo per recuperare informazioni dettagliate sullo stato di un'operazione di backup o ripristino delle licenze. Questa interfaccia viene fornita con gli eventi di stato generati durante le operazioni di backup e ripristino delle licenze.
ms.assetid: fbcd059f-13d9-4edb-8946-b55c9da6dca4
keywords:
- Formato Windows Media Interface IWMDRMLicenseBackupRestoreStatus
- Interfaccia IWMDRMLicenseBackupRestoreStatus-formato Windows Media, descritto
topic_type:
- apiref
api_name:
- IWMDRMLicenseBackupRestoreStatus
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a9db5d95daab78a506a3cc994fb9dd22153d0907
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338622"
---
# <a name="iwmdrmlicensebackuprestorestatus-interface"></a>Interfaccia IWMDRMLicenseBackupRestoreStatus

L'interfaccia **IWMDRMLicenseBackupRestoreStatus** fornisce un metodo per recuperare informazioni dettagliate sullo stato di un'operazione di backup o ripristino delle licenze.

Questa interfaccia viene fornita con gli eventi di stato generati durante le operazioni di backup e ripristino delle licenze. Durante il backup delle licenze vengono generati diversi eventi **MEWMDRMLicenseBackupProgress** , ognuno dei quali dispone di un'istanza associata di questa interfaccia. Lo stesso vale per gli eventi **MEWMDRMLicenseRestoreProgress** , che vengono generati durante il ripristino delle licenze.

Per recuperare un puntatore a un'istanza dell'interfaccia **IWMDRMLicenseBackupRestoreStatus** , è prima necessario chiamare il metodo **IMFMediaEvent:: GetValue** dell'evento Progress. Il valore recuperato dall'evento è un puntatore all'interfaccia **IUnknown** dell'oggetto che implementa l'interfaccia **IWMDRMLicenseBackupRestoreStatus** .

## <a name="members"></a>Membri

L'interfaccia **IWMDRMLicenseBackupRestoreStatus** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IWMDRMLicenseBackupRestoreStatus** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IWMDRMLicenseBackupRestoreStatus** dispone di questi metodi.



| Metodo                                                          | Descrizione                                                                                   |
|:----------------------------------------------------------------|:----------------------------------------------------------------------------------------------|
| [**GetStatus**](iwmdrmlicensebackuprestorestatus-getstatus.md) | Recupera informazioni dettagliate sullo stato di un'operazione di backup o ripristino delle licenze.<br/> |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfacce**](drm-interfaces.md)
</dt> </dl>

 

