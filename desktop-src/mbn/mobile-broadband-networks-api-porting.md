---
description: Questa sezione contiene il materiale di riferimento per il porting delle API Win32 Mobile Broadband deprecate nelle API Windows Runtime.
title: Linee guida per la portabilità delle API Win32 di Mobile Broadband Windows Runtime
ms.topic: reference
ms.date: 08/23/2021
ms.openlocfilehash: 4cbe0415e40f18d372fdd8b9089dbd4afe197b38
ms.sourcegitcommit: 8d7ce0c4827f8a4fd501cc6487f1a8360e944577
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/24/2021
ms.locfileid: "122767710"
---
# <a name="guidelines-for-porting-mobile-broadband-win32-apis-to-windows-runtime-apis"></a>Linee guida per la portabilità delle API Win32 di Mobile Broadband Windows Runtime

Questa tabella elenca le funzionalità Windows runtime per le API Win32 Mobile Broadband deprecate.

| **IMbnConnection** |  Funzionalità Windows Runtime equivalente |
| - | - |
| Connettere | ConnectivityManager.AcquireConnectionAsync |
| Disconnetti | ConnectionSession.Close |
| get \_ InterfaceID | MobileBroadbandAccount.NetworkAccountId |
| GetActivationNetworkError | MobileBroadbandNetwork.ActivationNetworkError |
| GetConnectionState | WwanConnectionProfileDetails.GetNetworkRegistrationState |
| GetVoiceCallState | MobileBroadbandNetwork.GetVoiceCallSupport, PhoneCallManager.IsCallActive |
| **IMbnConnectionEvents** | |
| OnConnectComplete | NetworkStateChangeEventDetails.HasNewWwanRegistrationState: dopo la notifica, lo stato di registrazione corrente può essere recuperato da WwanConnectionProfileDetails.GetNetworkRegistrationState. |
| OnConnectStateChange | NetworkStateChangeEventDetails.HasNewWwanRegistrationState: dopo la notifica, lo stato di registrazione corrente può essere recuperato da WwanConnectionProfileDetails.GetNetworkRegistrationState. |
| OnDisconnectComplete | NetworkStateChangeEventDetails.HasNewWwanRegistrationState: dopo la notifica, lo stato di registrazione corrente può essere recuperato da WwanConnectionProfileDetails.GetNetworkRegistrationState. |
| OnVoiceCallStateChange | PhoneCallManager.CallStateChanged |
| **IMbnConnectionProfile** | |
| Elimina | ConnectionProfile.TryDeleteAsync |
| GetConnectionProfile | NetworkAdapter.GetConnectedProfileAsync |
| GetConnectionProfiles | NetworkInformation.GetConnectionProfiles |
| **IMbnDeviceService** | |
| CloseCommandSession | MobileBroadbandDeviceServiceCommandSession.CloseSession |
| CloseDataSession | MobileBroadbandDeviceServiceDataSession.CloseSession |
| get \_ DeviceServiceID | MobileBroadbandDeviceService.DeviceServiceId |
| OpenCommandSession | MobileBroadbandDeviceService.OpenCommandSession |
| OpenDataSession | MobileBroadbandDeviceService.OpenDataSession |
| QueryCommand | MobileBroadbandDeviceServiceCommandSession.SendQueryCommandAsync |
| QuerySupportedCommands | MobileBroadbandDeviceService.SupportedCommands |
| SetCommand | MobileBroadbandDeviceServiceCommandSession.SendSetCommandAsync |
| WriteData | MobileBroadbandDeviceServiceDataSession.WriteDataAsync |
| **IMbnDeviceServicesContext** | |
| EnumerateDeviceServices | MobileBroadbandDeviceService.SupportedCommands |
| get \_ MaxCommandSize | MobileBroadbandModem.MaxDeviceServiceCommandSizeInBytes |
| get \_ MaxDataSize | MobileBroadbandModem.MaxDeviceServiceDataSizeInByte |
| GetDeviceService | MobileBroadbandModem.GetDeviceService |
| **IMbnDeviceServicesEvents** | |
| OnReadData | MobileBroadbandDeviceServiceDataSession.DataReceived |
| **Interfaccia IMbn** | |
| get \_ InterfaceID | MobileBroadbandAccount.NetworkAccountId |
| GetConnection | ConnectionSession ottenuta da AcquireConnectionAsync |
| GetHomeProvider | MobileBroadbandModem.GetCurrentConfigurationAsync |
| GetInterfaceCapability | MobileBroadbandAccount.CurrentDeviceInformation |
| GetReadyState | MobileBroadbandDeviceInformation.NetworkDeviceStatus |
| GetSubscriberInformation | MobileBroadbandAccount.CurrentDeviceInformation |
| InEmergencyMode | MobileBroadbandModem.IsInEmergencyCallMode |
| **IMbnInterfaceEvents** | |
| OnEmergencyModeChange | MobileBroadbandModem.IsInEmergencyCallModeChanged |
| OnReadyStateChange | MobileBroadbandNetworkRegistrationStateChange |
| OnSubscriberInformationChange | MobileBroadbandAccountUpdatedEventArgs.HasDeviceInformationChanged |
| **IMbnInterfaceManager** | |
| GetInterface | MobileBroadbandModem.CurrentAccount |
| **IMbnInterfaceManagerEvents** | |
| OnInterfaceArrival | MobileBroadbandAccountWatcher.AccountAdded |
| OnInterfaceRemoval | MobileBroadbandAccountWatcher.Account |
| **IMbnMultiCarrier** | |
| GetCurrentCellularClass | MobileBroadbandDeviceInformation.CellularClass |
| **IMbnMultiCarrierEvents** | |
| OnCurrentCellularClassChange | MobileBroadbandAccountUpdatedEventArgs.HasDeviceInformationChanged |
| **IMbnPin** | |
| Modifica | MobileBroadbandPin.ChangeAsync |
| Disabilita | MobileBroadbandPin.DisableAsync |
| Abilita | MobileBroadbandPin.EnableAsync |
| Immettere | MobileBroadbandPin.EnterAsync |
| get \_ PinFormat | MobileBroadbandPin.Format |
| get \_ PinLengthMax | MobileBroadbandPin.MaxLength |
| get \_ PinLengthMin | MobileBroadbandPin.MaxLength |
| get \_ PinMode | MobileBroadbandPin.Enabled |
| get \_ PinType | MobileBroadbandPin.Type |
| GetPinManager | MobileBroadbandDeviceInformation.PinManager |
| Sbloccare | MobileBroadbandPin.UnblockAsync |
| **IMbnPinManager** | |
| GetPin | MobileBroadbandPinManager.GetPin |
| GetPinList | MobileBroadbandPinManager.SupportedPins |
| GetPinState | MobileBroadbandPin.LockState |
| **IMbnPinManagerEvents** | |
| **IMbnRadio** | |
| get \_ SoftwareRadioState | Radio.GetRadiosAsync - Radio. State |
| SetSoftwareRadioState | Radio.SetStateAsync |
| **IMbnRadioEvents** | |
| OnRadioStateChange | Radio.StateChanged |
| **IMbnRegistration** | |
| GetAvailableDataClasses | MobileBroadbandDeviceInformation.DataClasses |
| GetCurrentDataClass | MobileBroadbandNetwork.RegisteredDataClass |
| GetPacketAttachNetworkError | MobileBroadbandNetwork.PacketAttachNetworkError |
| GetProviderID | MobileBroadbandNetwork.RegisteredProviderId |
| GetProviderName | MobileBroadbandNetwork.RegisteredProviderName |
| GetRegisterState | MobileBroadbandNetwork.NetworkRegistrationState |
| GetRegistrationNetworkError | MobileBroadbandNetwork.ActivationNetworkError |
| **IMbnRegistrationEvents** | |
| OnPacketServiceStateChange | MobileBroadbandNetworkRegistrationStateChange |
| OnRegisterStateChange | MobileBroadbandNetworkRegistrationStateChange |
| GetSignalStrength | ConnectionProfile.GetSignalBar/MobileBroadbandCellLte.ReferenceSignalReceivedPowerInDBm/ MobileBroadbandCellGsm.ReceivedSignalStrengthInDBm |
| **IMbnSignalEvents** | |
| **IMbnSms** | |
| GetSmsConfiguration | SmsDevice2.SmscAddress, SmsDevice2.CellularClass, None per CDMAShortMessageSize e MaxMessageIndex che non è necessario come API pubblica. |
| SetSmsConfiguration | SmsDevice2.SmscAddress, nessuno degli altri parametri è supportato |
| SmsSendCdma | SendMessageAndGetResultAsync con CellularClass in ISmsMessageBase |
| SmsSendCdmaPdu | SendMessageAndGetResultAsync con Messagetype e CellularClass in ISmsMessageBase |
| SmsSendPdu | SendMessageAndGetResultAsync con MessageType in ISmsMessageBase |
| **IMbnSmsConfiguration** | |
| get \_ ServiceCenterAddress | SmsDevice2.SmscAddress |
| get \_ SmsFormat | SmsDevice2.CellularClass |
| put \_ ServiceCenterAddress | SmsDevice2.SmscAddress |
| **IMbnSmsEvents** | |
| OnSmsNewClass0Message | SmsMessageRegistration.MessageReceived |
| OnSmsSendComplete | SmsSendMessageResult |
| **IMbnSmsReadMsgPdu** | |
| get \_ Message | SmsTextMessage2.Body |
| get \_ PduData | SmsTextmessage2.Body |
| **IMbnSmsReadMsgTextCdma** | |
| ottenere \_ l'indirizzo | SmsTextMessage2.From |
| get \_ EncodingID | SmsTextMessage2.Encoding |
| get \_ Message | SmsTextMessage2.Body |
| get \_ Timestamp | SmsTextMessage.2Timestamp |
| **IMbnSubscriberInformation** | |
| get \_ SimIccID | MobileBroadbandDeviceInformation.SimIccId |
| get \_ SubscriberID | MobileBroadbandDeviceInformation.SubscriberId |
| get \_ TelephoneNumbers | MobileBroadbandDeviceInformation.TelephoneNumbers |
