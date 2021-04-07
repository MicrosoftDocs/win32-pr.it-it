---
title: Proprietà della proprietà IMsRdpExtendedSettings
description: Contiene una proprietà denominata.
ms.assetid: 3acaeff9-1617-46c3-80c3-b87496b83670
ms.tgt_platform: multiple
keywords:
- Proprietà Servizi Desktop remoto proprietà
- Servizi Desktop remoto proprietà proprietà, interfaccia IMsRdpExtendedSettings
- Interfaccia IMsRdpExtendedSettings Servizi Desktop remoto, proprietà Property
topic_type:
- apiref
api_name:
- IMsRdpExtendedSettings.Property
- IMsRdpExtendedSettings.get_Property
- IMsRdpExtendedSettings.put_Property
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1eadc8ce59e5a2bd50a4e61ad75b5124b24c21b8
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/19/2020
ms.locfileid: "103745351"
---
# <a name="imsrdpextendedsettingsproperty-property"></a>IMsRdpExtendedSettings::P proprietà roperty

Contiene una proprietà denominata.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_Property(
  [in]          BSTR    bstrPropertyName,
  [in]          VARIANT *pValue
);

HRESULT get_Property(
  [in]          BSTR    bstrPropertyName,
  [out, retval] VARIANT *pValue
);
```



## <a name="property-value"></a>Valore proprietà

Valore della proprietà denominata.

| Nome proprietà | Tipo di dati | Access | Può essere modificato dopo l'avvio della connessione | Descrizione |
|----------|-----------|--------|-----------------------------------------|-------------|
| ConnectToChildSession | **\_bool VT** | Lettura/Scrittura | Sì | Impostando questa proprietà su **true** , il controllo client si connette alla sessione figlio nel computer locale anziché in un server remoto. Se questa proprietà è impostata su **true**, non è possibile connettersi a un server remoto perché tutte le connessioni vengono reindirizzate a localhost. Per ulteriori informazioni sulle sessioni figlio, vedere [sessioni figlio](child-sessions.md). |
| DisableCredentialsDelegation | **\_bool VT** | Lettura/Scrittura | No | Se **true**, le credenziali non vengono inviate al server remoto. |
| EnableFrameBufferRedirection | **\_bool VT** | Lettura/Scrittura | No | Se **true**, viene eseguito un tentativo di reindirizzamento del buffer del frame. Per una connessione loopback (lo stesso computer è sia client che Server), il reindirizzamento del buffer dei frame consente la condivisione della memoria per il buffer dei frame tra le sessioni. |
| EnableHardwareMode | **\_bool VT**  | Solo scrittura | No | Se **true**, viene effettuato un tentativo di assistenza hardware con la decodifica grafica. |
| IgnoreCursors | **\_bool VT** | Solo scrittura | No | Se **true**, i cursori inviati dal server remoto vengono ignorati. |
| ManualClipboardSyncEnabled | **\_bool VT** | Lettura/Scrittura | Sì | L'impostazione di questa proprietà su **true** indica che gli Appunti locali e remoti non verranno mantenuti sincronizzati automaticamente. È invece necessario utilizzare l'interfaccia [**IMsRdpClipboard**](imsrdpclipboard.md) per sincronizzare i formati degli Appunti dagli Appunti locali negli Appunti remoti e negli Appunti remoti negli Appunti locali. |
| ZoomLevel | **_\_UI4 VT_* | Lettura/Scrittura | Sì | Implementa la funzionalità di zoom utilizzando il controllo ActiveX RDP. La funzionalità di zoom è disponibile dal menu di **sistema** di RDP. La proprietà **ZoomLevel** non ha alcun effetto in modalità RemoteApp e in modalità schermo intero. [**IMsRdpClientAdvancedSettings:: SmartSizing**](imsrdpclientadvancedsettings-smartsizing.md) e **ZoomLevel** si escludono a vicenda. |

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8<br/>                                                                                                                                                                                                                                                                                           |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                                                                                                                                                                                                                                                 |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                         |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                         |
| CLSID<br/>                    | CLSID \_ MsRdpClient7NotSafeForScripting è definito come 54d38bf7-b1ef-4479-9674-1bd6ea465258<br/> CLSID \_ MsRdpClient8NotSafeForScripting è definito come A3BC03A0-041d-42e3-AD22-882B7865C9C5<br/> CLSID \_ MsRdpClient9NotSafeForScripting è definito come 8B918B82-7985-4c24-89DF-C33AD2BBFBCD<br/> |
| IID<br/>                      | IID \_ IMsRdpExtendedSettings è definito come 302D8188-0052-4807-806A-362B628F9AC5<br/>                                                                                                                                                                                                                      |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsRdpExtendedSettings**](imsrdpextendedsettings.md)
</dt> </dl>

 

 





