---
title: Proprietà IMsRdpExtendedSettings
description: Contiene una proprietà denominata.
ms.assetid: 3acaeff9-1617-46c3-80c3-b87496b83670
ms.tgt_platform: multiple
keywords:
- Proprietà Servizi Desktop remoto
- Proprietà property Servizi Desktop remoto , interfaccia IMsRdpExtendedSettings
- Interfaccia IMsRdpExtendedSettings Servizi Desktop remoto , proprietà
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
ms.openlocfilehash: 7deeb0e4d6d0f393bae09bacc9ff6709defe51bf6ca6128cbeb64e2f4f6e35cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119138504"
---
# <a name="imsrdpextendedsettingsproperty-property"></a>Proprietà IMsRdpExtendedSettings::P roperty

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
| ConnectToChildSession | **VT \_ BOOL** | Lettura/Scrittura | Sì | Se si imposta questa **proprietà su True,** il controllo client si connette alla sessione figlio nel computer locale anziché in un server remoto. Se questa proprietà è impostata **su true,** non è possibile connettersi a un server remoto perché tutte le connessioni vengono reindirizzate a localhost. Per altre informazioni sulle sessioni figlio, vedere [Sessioni figlio](child-sessions.md). |
| DisableCredentialsDelegation | **VT \_ BOOL** | Lettura/Scrittura | No | Se **True,** le credenziali non vengono inviate al server remoto. |
| EnableFrameBufferRedirection | **VT \_ BOOL** | Lettura/Scrittura | No | Se **True,** viene effettuato un tentativo di reindirizzamento del buffer dei frame. Per una connessione loopback (lo stesso computer è sia client che server) il reindirizzamento del buffer dei frame consente la condivisione della memoria per il buffer di frame tra le sessioni. |
| EnableHardwareMode | **VT \_ BOOL**  | Sola scrittura | No | Se **True,** viene effettuato un tentativo di decodifica dell'hardware per la decodifica grafica. |
| IgnoreCursors | **VT \_ BOOL** | Sola scrittura | No | Se **True,** i cursori inviati dal server remoto vengono ignorati. |
| ManualClipboardSyncEnabled | **VT \_ BOOL** | Lettura/Scrittura | Sì | L'impostazione di **questa proprietà** su True significa che gli Appunti locali e remoti non verranno mantenuti automaticamente sincronizzati. È invece [**necessario usare l'interfaccia IMsRdpClipboard**](imsrdpclipboard.md) per sincronizzare i formati degli Appunti dagli Appunti locali agli Appunti remoti e agli Appunti remoti negli Appunti locali. |
| ZoomLevel | ***Interfaccia utente \_ VT4** | Lettura/Scrittura | Sì | Implementa la funzionalità Zoom usando il controllo ActiveX RDP. La funzionalità Zoom è disponibile nel menu **Sistema** di RDP. La **proprietà ZoomLevel** non ha alcun effetto in modalità RemoteApp e modalità schermo intero. [**IMsRdpClientAdvancedSettings::SmartSizing**](imsrdpclientadvancedsettings-smartsizing.md) e **ZoomLevel** si escludono a vicenda. |

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8<br/>                                                                                                                                                                                                                                                                                           |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                                                                                                                                                                                                                                                 |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                         |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                         |
| CLSID<br/>                    | CLSID \_ MsRdpClient7NotSafeForScripting è definito come 54d38bf7-b1ef-4479-9674-1bd6ea465258<br/> CLSID \_ MsRdpClient8NotSafeForScripting è definito come A3BC03A0-041D-42E3-AD22-882B7865C9C5<br/> CLSID \_ MsRdpClient9NotSafeForScripting è definito come 8B918B82-7985-4C24-89DF-C33AD2BBFBCD<br/> |
| IID<br/>                      | IMsRdpExtendedSettings IID è definito come \_ 302D8188-0052-4807-806A-362B628F9AC5<br/>                                                                                                                                                                                                                      |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsRdpExtendedSettings**](imsrdpextendedsettings.md)
</dt> </dl>

 

 





